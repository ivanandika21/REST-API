# Mencoba Public API

## Siapkan terlebih dahulu html dengan search input beserta button

## Buat script menggunakan Javascript
```
function searchMovie() {
  // tambahan untuk mengosongkan movie list saat search dilakukan lebih dari 1 kali
  $('#movie-list').html('');
  
  $.ajax({
    url: 'http://omdbapi.com',
    type: 'get',
    dataType: 'json',
    data: {
      'apikey': 'abcdefgh',
      's': $('#search-input').val()
    },
    success: function(result) {
      if(result.Response == "True"){
        let movies = result.Search;
        
        $.each(movies, function(i, data){
          // buat card disini
          $('#movie-list').append(`
          <p>` + data.Poster + `</p>
          <p>` + data.Title + `</p>
          <p>` + data.Year + `</p>
          <a href="#" class="card-link see-detail" data-toggle="modal" data-target="#exampleModal" data-id="` + data.imdbID + `">See Detail</a>
          `);
        });
        
        // tambahan untuk mengosongkan search input saat ada result
        $('#search-input').val('');
      } else {
        $('#movie-list').html(`
        <div class="col">
          <h1 class="text-center">` + result.Error + `</h1>
        </div>  
        `)
      }
    }
  });
}
```

## Panggil fungsi searchMovie()
```
#('#search-button').on('click', function() {
  searchMovie();
});
```

## Agar saat menekan enter dapat melakukan search
```
$('#search-input').on('keyup', function(e){
  if(e.keyCode === 13){
    searchMovie()
  }
});
```

## Tambahan untuk membuka modal See Detail
```
// Terjadi event binding pada .see-detail karena sebelum movie list tampil, on click sudah dipasangkan pada element .see-detail padahal belum ada
// Solusinya adalah mencari terlebih dahulu element diluarnya yaitu #movie-list baru cari .see-detail didalamnya, lalu jalankan fungsi
$('#movie-list').on('click', '.see-detail', function() {
  $.ajax({
    url: 'http://omdbapi.com',
    type: 'get',
    dataType: 'json',
    data: {
      'apikey': 'abcdefgh',
      'i': $(this).data('id'); // this adalah tombol See Detail yang di klik
    },
    success: function(movie) {
      if(movie.Response === "True"){
        $('.modal-body').html(`
          <div class="row">
            <div class="col-md-4">
              <img src="` + movie.Poster + `" class="img-fluid">
            </div>
            <div class="col-md-8">
              <ul>
                <li>` + movie.Title + `</li>
                <li>` + movie.Released + `</li>
                <li>` + movie.Genre + `</li>
                <li>` + movie.Director + `</li>
                <li>` + movie.Actors + `</li>
              </ul>
            </div>
          </div>
        `)
      }
    }
  });
});
```
