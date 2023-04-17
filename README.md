# ODEV 3

Merhabalar,

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

    country tablosunda bulunan country sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri ile sonlananları sıralayınız.
    country tablosunda bulunan country sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri ile sonlananları sıralayınız.
    film tablosunda bulunan title sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin 'T' karakteri içeren film isimlerini sıralayınız.
    film tablosunda bulunan tüm sütunlardaki verilerden title 'C' karakteri ile başlayan ve uzunluğu (length) 90 dan büyük olan ve rental_rate 2.99 olan verileri sıralayınız.

Kolay Gelsin.

# CEVAPLAR

## 1.Soru:

SELECT country FROM country
WHERE country LIKE 'A%a';

"Algeria"
"American Samoa"
"Angola"
"Anguilla"
"Argentina"
"Armenia"
"Australia"
"Austria"

## 2.Soru:

SELECT country FROM country
WHERE country LIKE '%_____n';

"Afghanistan"
"Azerbaijan"
"Bahrain"
"Cameroon"
"Kazakstan"
"Liechtenstein"
"Pakistan"
"Runion"
"Russian Federation"
"Sweden"
"Taiwan"
"Turkmenistan"

## 3.Soru:

SELECT title FROM film
WHERE title ILIKE '%t%t%t%t';

"Haunted Antitrust"
"Potter Connecticut"

## 4.Soru:

SELECT * FROM film
WHERE title LIKE 'C%' AND length > 90 AND rental_rate = 2.99;

"Campus Remember"
"Carol Texas"
"Cause Date"
"Chaplin License"
"Chitty Lock"
"Chocolate Duck"
"Cider Desire"
"Clones Pinocchio"
"Clueless Bucket"
"Core Suit"
"Color Philadelphia"
"Confused Candles"
"Conspiracy Spirit"
"Contact Anonymous"
"Cowboy Doom"
"Crazy Home"
"Crossroads Casualties"
"Crusade Honey"
"Crystal Breaking"
"Cyclone Family"

