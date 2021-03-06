# HTML Validator
- محدودیت زمان: ۱ ثانیه
- محدودیت حافظه: ۲۵۶ مگابایت

احتمالا با زبان قالب بندی متن یا همان اچ تی ام ال آشنایی داشته باشید.
از این زبان برای ساخت صفحات وب استفاده می‌شود.
در این سوال می‌خواهیم کدی بزنیم که یک کد نوشته شده به زبان اچ تی ام ال را به عنوان ورودی بگیرد و بررسی کند که آیا قواعد این زبان در کد رعایت شده است یا خیر.

برای یادگیری بیشتر این زبان و طراحی صفحات وب می‌توانید به [این لینک](https://www.w3schools.com/html/default.asp) مراجعه کنید.

به عنوان مثال متن زیر یک کد ساده و معتبر در زبان اچ تی ام ال می‌باشد:
```html
<html lang="en">
    <head>
        <title>Page Title</title>
    </head>
    <body>

        <h1>This is a Heading</h1>
        <p>This is a paragraph.</p>

    </body>
</html>
```
یک کد اچ تی ام ال شامل مجموعه ای از [تگ‌ها](https://www.w3schools.com/html/html_elements.asp)ست که  هر تگ به یکی از شکل های زیر است:
- تگ دوتایی:
`<p> content </p>`
- تگ تکی:
`<img />`

تگ‌های دوتایی می‌توانند یک خصوصیت را بر روی متن یا محتوایی که درون آنها قرار دارند اعمال کنند.  یعنی مثلا خروجی کد زیر به صورت مشخص شده خواهد بود:

```html
<b>bold text</b>
<i>italic text</i>
``` 
**bold text**
_italic text_

همچنین یک متن می‌تواند میان چندین تگ قرار بگیرد و در این صورت ویژگی‌های همهٔ آن تگ‌ها را با هم می‌پذیرد:
```html
<b> <i> bold and italic text </i> </b>
```
**_bold and italic text_**

اما نکته مهمی که باید توجه داشت این است که وقتی در میان چندین تگ هستیم، همیشه آخرین تگی که باز شده -و هنوز بسته نشده- باید بسته شود. یعنی مثال بالا یک مثال معتبر است اما مثال زیر یک مثال نامعتبر است:
```html
<b>
<i>
</b>
</i>
```
چون اول تگ بلد باز و بعد تگ ایتالیک. اما تگ بلد قبل از بسته شدن تگ ایتالیک بسته شده.

توجه کنید که این قسمت دقیقا مانند پرانتز گذاری است. یعنی اگر یک عبارت ریاضی شامل () و [] و {} باشد همیشه آخرین چیزی که باز شده -و هنوز بسته نشده- باید بسته شود.

علاوه بر این‌ها هر تگ می‌تواند خصوصیاتی داشته باشد که در تگ آغازین آن به صورت زیر مشخص می‌شوند:
```html
<tagname attribute1="value1" attribute2="value2">
</tagname>
```
برای تگ‌های تکی هم به صورت زیر است:
```html
<tagname attribute1="value1" attribute2="value2"/>
```
حال می‌خواهیم کدی بنویسیم که نحوهٔ باز و بسته شدن تگ‌ها را بررسی کند و مشخص کند که کد ما از این نظر صحیح است یا خیر.
#### ورودی :
ورودی شامل یک رشته اچ تی ام ال است که در چند خط داده می‌شود. تضمین می‌شود که آخرین خط کد همواره تگ بستهٔ اچ تی ام ال است. یعنی عبارت زیر:
```html
</html>
``` 
#### خروجی:
اگر ترتیب باز و بسته شدن تگ‌ها صحیح است باید چاپ کنیم بله. وگرنه خیر.  
`YES` و `NO`

### مثال ۱:
#### ورودی:
```html
<html lang="en">
<head>
    <title>
        My Page        
    </title>
</head>
<body dir="ltr">
<p>This is a paragraph</p>
<div>This is a div</div>
</body>
</html>
```
#### خروجی:
```html
YES
```
### مثال ۲:
#### ورودی:
```html
<html>
<head>
    <meta charset="utf-8"/>
</head>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.

</body>
</html>
```
#### خروجی:
```html
NO
```
توضیح: تگ پاراگراف بسته نشده برای همین ورودی نامعتبر است.
