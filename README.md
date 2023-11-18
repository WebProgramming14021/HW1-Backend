<div dir="rtl">

### توضیحات کلی:

در این تمرین، شما باید وب‌سایت یک دانشگاه را مدل‌سازی کنید. هدف از این تمرین درک عمیق‌تر از مدل‌سازی داده و استفاده از مفاهیم مختلف جنگو مانند روابط بین مدل‌ها است.

</div>

<div dir="rtl">

### مراحل تمرین:


1. **تعریف مدل‌ها**:
    - `Student`: با فیلدهای `first_name`, `last_name`, `student_number`, `enrollment_year`, `major`
    - `Professor`: با فیلدهای `first_name`, `last_name`, `staff_number`, `hiring_date`, `department`
    - `Course`: با فیلدهای `course_name`, `course_code`, `unit_count`, `offered_by`(این یک رابطه به `Professor` است)
    - `Enrollment`: این مدل نشان‌دهنده ثبت نام دانشجو در درس است و باید دارای روابط به `Student` و `Course` باشد. همچنین فیلدی به نام `semester` نیز داشته باشد.
    - `Department`: با فیلدهای `name`, `head_of_department`(این یک رابطه به `Professor` است)

</div>

<div dir="rtl">

2. **تعریف روابط**:
    - یک دانشجو می‌تواند در چندین درس ثبت‌نام کند و همچنین یک درس می‌تواند چندین دانشجو داشته باشد؛ بنابراین بین `Student` و `Course` یک رابطه ManyToMany ایجاد می‌شود که از مدل `Enrollment` به عنوان جدول واسط استفاده می‌شود.
    - هر درس توسط یک استاد ارائه می‌شود، بنابراین بین `Course` و `Professor` یک رابطه ForeignKey وجود دارد.
    - هر دپارتمان یک رئیس دپارتمان دارد که یک استاد است، بنابراین بین `Department` و `Professor` یک رابطه ForeignKey وجود دارد.

</div>

<div dir="rtl">

3. **ویژگی‌های اضافی**:
    - برای هر مدل، متدهای `__str__` را تعریف کنید تا نمایش مناسبی از هر رکورد در ادمین جنگو داشته باشید.
    - استفاده از ویژگی‌های مانند `unique` و `choices` برای فیلدهای مناسب.
    - ایجاد مدل‌های اضافی مانند `Classroom`, `Schedule`, یا `Assignment` برای پیچیده‌تر کردن مدل‌سازی وب‌سایت.

</div>

<div dir="rtl">

4. **مستندات**:
    - در کد خود تا جای ممکن کامنت مناسب قرار دهید تا برای تحویل‌گیرنده‌ی این تمرین، بدون توضیح شما، کد کاملا قابل درک و خوانا باشد. همچنین یک داکیومنت خلاصه از نحوه‌ی پیاده‌سازی کد تهیه و در کنار فایل خود کد، آپلود کنید.

</div>
<div dir="rtl">

### خروجی: یک فایل `model.py` به عنوان خروجی این تمرین آپلود کنید در کوئرا.

</div>
