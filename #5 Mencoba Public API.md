# Mencoba Public API

## Siapkan terlebih dahulu html dengan search input beserta button

## Buat script menggunakan Javascript
```
#('#search-button').on('click', function() {
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
      } else {
        $('#movie-list').html(`
        <div class="col">
          <h1 class="text-center">` + result.Error + `</h1>
        </div>  
        `)
      }
    }
  });
});
```
