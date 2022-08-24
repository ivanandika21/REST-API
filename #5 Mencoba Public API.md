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
