/_  
/_ SELECT _ FROM InvoiceLine i JOIN InvoiceLine il ON
i.invoiceId = il.invoiceId where il.unitPrice > 0.99;
SELECT i.InvoiceDate, c.FirstName, c.LastName, i.Total
FROM Invoice i
JOIN Customer c ON i.CustomerId = c.CustomerId
SELECT c.FirstName, c.LastName, e.FirstName, e.LastName FROM Customer C
JOIN Employee e ON c.SupportRepId = e.EmployeeID; _/
/_ SELECT Al.Title, AR.Name FROM Album Al JOIN Artist Ar on Al.ArtistID =
Ar.ArtistID;
_/
/\*
SELECT Pl.TrackId FROM PlaylistTrack Pl JOIN PlayList P on Pl.Playlistid =
P.Playlistid WHERE P.Name = 'Music';

SELECT t.Name
FROM Track t
JOIN PlaylistTrack pt ON pt.TrackId = t.TrackId
WHERE pt.PlaylistId = 5;
_/
/_
/_ SELECT t.name, p.Name
FROM Track t
JOIN PlaylistTrack pt ON t.TrackId = pt.TrackId
JOIN Playlist p ON pt.PlaylistId = p.PlaylistId; _/

/_ SELECT _ FROM Invoice WHERE InvoiceId IN ( SELECT InvoiceId FROM InvoiceLine
WHERE UnitPrice > 0.99);



SELECT \*
FROM PlaylistTrack
WHERE PlaylistId IN ( SELECT PlaylistId FROM Playlist WHERE Name = "Music" );

SELECT Name
FROM Track
WHERE TrackId IN ( SELECT TrackId FROM PlaylistTrack WHERE PlaylistId = 5 );

FROM Track
WHERE GenreId IN ( SELECT GenreId FROM Genre WHERE Name = "Comedy" );

SELECT \*
FROM Track
WHERE AlbumId IN ( SELECT AlbumId FROM Album WHERE Title = "Fireball" );

SELECT _
FROM Track
WHERE AlbumId IN (
SELECT AlbumId FROM Album WHERE ArtistId IN (
SELECT ArtistId FROM Artist WHERE Name = "Queen"
)
); _/
/\*
UPDATE Customer
SET Fax = null
WHERE Fax IS NOT null;

UPDATE Customer
SET Company = "Self"
WHERE Company IS null;

UPDATE Customer
SET LastName = "Thompson"
WHERE FirstName = "Julia" AND LastName = "Barnett";
UPDATE Customer
SET SupportRepId = 4
WHERE Email = "luisrojas@yahoo.cl";
UPDATE Track
SET Composer = "The darkness around us"
WHERE GenreId = ( SELECT GenreId FROM Genre WHERE Name = "Metal" )
AND Composer IS null; _/
/_
SELECT COUNT(\*), g.Name FROM Track t JOIN Genre g ON t.GenreId GROUP BY g.name;

SELECT Count(_), g.Name
FROM Track t
JOIN Genre g ON g.GenreId = t.GenreId
WHERE g.Name = 'Pop' OR g.Name = 'Rock'
GROUP BY g.Name;
SELECT ar.Name, Count(_)
FROM Artist ar
JOIN Album al ON ar.ArtistId = al.ArtistId
GROUP BY al.ArtistId;
SELECT DISTINCT Composer
FROM Track;
SELECT DISTINCT Composer
FROM Track;
SELECT DISTINCT Company
FROM Customer;
DELETE
FROM practice_delete
WHERE Type = "bronze";
DELETE
FROM practice_delete
WHERE Type = "silver";
DELETE
FROM practice_delete
WHERE Value = 150; \*/
