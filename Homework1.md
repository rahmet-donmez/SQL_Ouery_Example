# SORULAR
Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1-film tablosunda bulunan title ve description sütunlarındaki verileri sıralayınız.

2-film tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (length) 60 dan büyük VE 75 ten küçük olma koşullarıyla sıralayınız.

3-film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.

4-customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?

5-film tablosundaki uzunluğu(length) 50 ten büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.

# CEVAPLAR

```
 Select title,description from public.film
```
```
Select * from public.film where length>60 and length<70
```
```
Select * from public.film where rental_rate=0.99 and (replacement_cost=12.99 or replacement_cost=28.99)
```
```
Select last_name from public.customer where first_name='Mary'
```
```
Select * from public.film where NOT length>50  and NOT (rental_rate=2.99 OR rental_rate=4.99)
```
