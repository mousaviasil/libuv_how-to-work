<p align="right">به نام خدا</p>
<p align="right"> برای کار کردن با کتابخانه «لیب‌یووی» چالش‌های زیادی داشتم  با توجه به اینکه این کتابخانه امکانات جالبی  مهیا کرده احساس کردم نیاز به معرفی روانتری دارد.</p>
<p align="right"> مطالبی که در اینجا می نویسم تجاربی است که در حین آشنایی با مفاهیم اولیه و راه اندازی  کتابخانه با آنها مواجه شدم . خوشحال می‌شوم در این مسیر من را همراهی کنید و در فهم و یادگیری سخاوتمندانه همراه یکدیگر باشیم.</p>
<hr>
<p align="right"><a href="#titel_1">معرفی کتابخانه و مفاهیم پایه</a></p>
<p align="right"><a href="#titel_2">راه‌اندازی و انتخاب ادیتور مناسب</a></p>
<p align="right"><a href="#titel_3">کدهای نمونه</a></p>
<hr>
<p align="right" id="titel_1"> معرفی کتابخانه و مفاهیم پایه</p>
<p dir="rtl" align="right"> کتابخانه ای بنام libuv به زبان c  نوشته شده که ویژگیهای خاصی برای علاقمندان به کارهای سیستمی دارد. کتابخانه libuv ویژگیهای ذیل دارد:
<p dir="rtl" align="right">مستقل از سیستم عامل (روی هر سیستم عاملی کار می کند و بدلیل عدم وابستگی به سیستم عامل بسیار سریع است)
رویداد گرا ( هر اتفاقی بیافتد بلافاصله  با خبر می شوید. کارهای I/O  بلوکه کننده نیستند  و به صورت غیر همگام کارها انجام می شود)
این کتابخانه با ویژگی عالی  cross-platform بودن و عدم مسدود کردن  در حین انجام کارهای I/O و مستقل از سسیتم عامل باعث شده فضای مناسبی برای تسریع در کارها  ایجاد کرده و یک زیر ساخت مناسبی برای کد نویسی سیستمی شده است. </p>
<p dir="rtl" align="right">هسته کاری libuv بر اساس event-loop و call back  که روی I/O مطرح می شود. مسولیت جمع آوری event ها از سیستم عامل و یا نظارت بر دیگر event ها توسط libuv انجام می شود. کاربر call back ها را ثبت می کند تا زمانی که event اتفاق بیافتد.
</p><p dir="rtl" align="right">
می دانیم برای اینکه یک کار I/O انجام شود  پردازنده یک زمانی بیکار خواهد بود و اتلاف زمانی تا اجرای کامل دستور العمل خواهیم داشت. راهکار threading  برای کاهش زمان بیکاری پردازنده استفاده می شود. event-loopروش دیگری که توسط libuv مطرح شده که باعث اجرای آسنکرون غیر بلوکه کننده می شود.</p>
<p dir="rtl" align="right">کدنویسی با کمک libuv رعایت اصولی را می طلبد که باید دقت شود.</p>
<p dir="rtl" align="right"> افزودن کتابخانه uv.h به کد اولین کاری که باید انجام شود.</p>
<p dir="rtl" align="right">تخصیص حافظه برای event-loop</p>
<p dir="rtl" align="right">مقدار دهی اولیه صف event-loop.</p>
<p dir="rtl" align="right">کدهای برنامه....</p>
<p dir="rtl" align="right">اجرا از صف event-loop</p>
<p dir="rtl" align="right">حذف مقدار دهی اولیه صف</p>
<p dir="rtl" align="right">حذف حافظه تخصیص داده شده</p>


#include <uv.h>

main()

{

uv_loop_t *loop= malloc(size of(uv_loop_t));

uv_loop_init(loop);

..

uv_run(loop,UV_RUN_DEFAULT);

uv_loop_close(loop);

free(loop) 
}

<p align="right" id="titel_2">راه اندازی و انتخاب ادیتور مناسب</p>


<p align="right" id="titel_3">نمونه کدهای نوشته شده</p>
http://mousaviasil.blogfa.com/category/1

