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
        
      } else {
        $('#movie-list').html('<h1 class="text-center">' + result.Error + '</h1>')
      }
    }
  });
});
```
