# SoftwareLab_Az3


## SOLID دستور آزمایش

### گام ۱: افزودن یک روش پیام رسانی دیگر

1.	بدون آن که متدی را از واسط Messaging Service حذف کنید ، یک سرویس دیگری را به منظور ارسال پیام از تلگرام با داشتن آیدی مبدا و آیدی مقصد ایجاد کنید - به تبع آن لازم است که یک زیر کلاس برای Message به نام Telegeram Message اضافه کنید که در آن سرویس مورد استفاده قرار گیرد.
2.	سپس یک تابع برای ارسال پیام تلگرامی در واسط Message Service اضافه کنید.
3.	در بدنه‌ی تابع مذکور - مشابه با دیگر توابع پیاده سازی شده -  از یک دستور چاپ ساده بر روی صفحه نمایش استفاده کنید.
4.	در ادامه، سعی کنید که قابلیت ارسال پیام تلگرامی را نیز به برنامه اضافه کنید؛ یعنی کاری کنید که کاربر بتواند در قالب روش سوم پیام خود را با داشتن آیدی مبدا و آیدی مقصد و متن پیام، ارسال کند.
5.	تغییراتی را که در کد فعلی برنامه می‌دهید، در جدول زیر ثبت کنید و در نهایت تعداد کل تغییرات را اعلان کنید.
    - توجه: مواردی که به عنوان تغییرات باید اعلان شود شامل این موارد هستند:
      1. ساخت کلاس جدید
      2. افزودن تابع جدید به کلاس و یا واسط (برای توابع جدید صرفا اعلام تغییر کنید)
      3. هر خطوط پیاپی‌ای که در تابع main و برای افزودن یک قابلیت جدید اضافه می‌کنید. به عنوان مثال اگر سه خط را به منظور تشخیص نوع پیام اضافه می‌کنید، آن سه خط را در قالب یک تغییر اعلام کنید (البته جزییات آن را در ستون «شرحی کوتاه از تغییر» توضیح دهید).

<table dir='rtl'>
<tbody>
<tr>
<td width="64">
<p><strong>ردیف</strong></p>
</td>
<td width="198">
<p><strong>محل اعمال تغییرات (کلاس/واسط)</strong></p>
</td>
<td width="141">
<p><strong>عنوان تغییر</strong></p>
</td>
<td width="292">
<p><strong>شرحی کوتاه از تغییر</strong></p>
</td>
</tr>
<tr>
<td width="64">
<p><strong>1</strong></p>
</td>
<td width="198">
<p>MessageService</p>
</td>
<td width="141">
<p>افزودن تابع ارسال پیام تلگرامی</p>
</td>
<td width="292">
<p>افزودن یک تابع void با عنوان sendTelegramMessage</p>
</td>
</tr>

<tr>
<td width="64">
<p><strong>2</strong></p>
</td>
<td width="198">
<p>TelegramMessageService</p>
</td>
<td width="141">
<p>اضافه کردن کلاس</p>
</td>
<td width="292">
<p>این کلاس مربوط به توابع سرویس‌دهنده به پیام‌رسانی از طریق تلگرام است</p>
</td>
</tr>

<tr>
<td width="64">
<p><strong>3</strong></p>
</td>
<td width="198">
<p>TelegramMessage </p>
</td>
<td width="141">
<p>اضافه کردن کلاس</p>
</td>
<td width="292">
<p>این کلاس مدل مربوط به پیام‌رسان تلگرام است که برای get و set کردن id مربوط به مبدا و مقصد است.</p>
</td>
</tr>

<tr>
<td width="64">
<p><strong>4</strong></p>
</td>
<td width="198">
<p>SmsMessageService </p>
</td>
<td width="141">
<p>اضافه کردن تابع sendTelegramMessage  </p>
</td>
<td width="292">
<p>تابع با بدنه‌ی خالی اضافه می‌کنیم  که override شده.</p>
</td>
</tr>

<tr>
<td width="64">
<p><strong>5</strong></p>
</td>
<td width="198">
<p>EmailMessageService </p>
</td>
<td width="141">
<p>اضافه کردن تابع sendTelegramMessage  </p>
</td>
<td width="292">
<p>تابع با بدنه‌ی خالی اضافه می‌کنیم  که override شده.</p>
</td>
</tr>

<tr>
<td width="64">
<p><strong>6</strong></p>
</td>
<td width="198">
<p>TelegramMessageService </p>
</td>
<td width="141">
<p>اضافه کردن تابع به TelegramMessageService	</p>
</td>
<td width="292">
<p>	تابع sendTelegramMessage را پیاده‌سازی میکنیم.</p>
</td>
</tr>

<tr>
<td width="64">
<p><strong>7</strong></p>
</td>
<td width="198">
<p>TelegramMessageService </p>
</td>
<td width="141">
<p>اضافه کردن تابع به TelegramMessageService	</p>
</td>
<td width="292">
<p>	تابع validateTelegramID را پیاده‌سازی میکنیم.</p>
</td>
</tr>

<tr>
<td width="64">
<p><strong>8</strong></p>
</td>
<td width="198">
<p>TelegramMessageService </p>
</td>
<td width="141">
<p>اضافه کردن توابع به TelegramMessageService	</p>
</td>
<td width="292">
<p>	توابع sendEmailMessage و sendSmsMessage را با بدنه‌ی خالی اضافه میکنیم. </p>
</td>
</tr>


<tr>
<td width="64">
<p><strong>9</strong></p>
</td>
<td width="198">
<p>Main </p>
</td>
<td width="141">
<p>اضافه کردن prompt جدید و مدیریت آن   </p>
</td>
<td width="292">
<p>  علاوه‌بر prompt یک case جدید هم به switch_case اضافه میکنیم تا محتوای آن را مشخص کنیم.</p>
</td>
</tr>

<tr>
<td width="64">
<p><strong>10</strong></p>
</td>
<td width="198">
<p>Main </p>
</td>
<td width="141">
<p>اضافه کردن instance جدید برای پیام تلگرامی   </p>
</td>
<td width="292">
<p>یک instance از کلاس TelegramMessageService در صورت اینکه message == telegramMessage</p>
</td>
</tr>


</tbody>
</table>

مجموع تعداد تغییرات: 10
