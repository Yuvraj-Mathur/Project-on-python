<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shaktipeeth Vedic E-Library</title>
    <link rel="stylesheet" href="Look.css">
</head>
    <body>
        <header>
            <h1>Welcome to the E-Library</h1>
        </header>
        
        <div class="container">
            <div class="search-box">
                <input type="text" id="search" placeholder="Search for books..." onkeyup="searchBooks()">
            </div>
            <div class="book-list" id="bookList">
                <div class="book">Shruti</div>
                    
                <div class="book">Smriti</div>
            </div>
        </div>

        <script>
            function searchBooks() {
                let input = document.getElementById('search').value.toLowerCase();
                let books = document.getElementsByClassName('book');
            
                for (let i = 0; i < books.length; i++) {
                    let title = books[i].innerText.toLowerCase();
                    if (title.includes(input)) {
                        books[i].style.display = "block";
                    } else {
                        books[i].style.display = "none";
                    }
                }
            }
        </script>
    </body>
</html>
