# Welcome to GitHub Desktop!

This is your README. READMEs are where you can communicate what your project is and how to use it.

Write your name on line 6, save it, and then head back to GitHub Desktop.
Bayniyazov Abdiqadir
Ushbu misolda biz << - operatorini joriy qilamiz, u yordamida muhitdan ob'ektga qiymat berish uchun ishlatilishi mumkin. Quyida raqamli vektorni saqlaydigan va uning o'rtacha qiymatini keshlaydigan maxsus ob'ektni yaratish uchun ishlatiladigan ikkita funktsiya mavjud.

Birinchi funktsiya, makeVector maxsus "vektor" yaratadi, bu haqiqatan ham funktsiyani o'z ichiga olgan ro'yxat

vektorning qiymatini o'rnating
vektorning qiymatini oling
o'rtacha qiymatini o'rnating
o'rtacha qiymatini oling
12018-04-02 121 2345678910111213
makeVector <- function(x = numeric()) {
        m <- NULL
        set <- function(y) {
                x <<- y
                m <<- NULL
        }
        get <- function() x
        setmean <- function(mean) m <<- mean
        getmean <- function() m
        list(set = set, get = get,

Quyidagi funktsiya yuqoridagi funktsiya bilan yaratilgan maxsus "vektor" ning o'rtacha qiymatini hisoblab chiqadi. Biroq, avval o'rtacha hisoblab chiqilganligini tekshiradi. Agar shunday bo'lsa, u o'rtacha keshdan oladi va hisoblashni o'tkazib yuboradi. Aks holda, u ma'lumotlar o'rtacha qiymatini hisoblaydi va setmean funktsiyasi orqali keshdagi o'rtacha qiymatini belgilaydi.

12018-04-02 121 234567891011
cachemean <- function(x, ...) {
        m <- x$getmean()
        if(!is.null(m)) {
                message("getting cached data")
                return(m)
        }
        data <- x$get()
        m <- mean(data, ...)
        x$setmean(m)
        m

Topshiriq: Matritsaning teskarisini keshlash
Kamroq 
Matritsaning teskari o'zgarishi odatda qimmatga tushadigan hisob-kitob bo'lib, matritsani teskari keshlash uchun uni qayta-qayta hisoblashdan ko'ra ko'proq foyda keltirishi mumkin (shuningdek, matritsaning teskari variantiga alternativalar mavjud, biz bu erda muhokama qilmaymiz). Sizning topshirig'ingiz matritsaning teskarisini keshlaydigan juft funktsiyalarni yozishdir.

Quyidagi funktsiyalarni yozing:

makeCacheMatrix: Ushbu funktsiya teskari keshlashi mumkin bo'lgan maxsus "matritsa" ob'ektini yaratadi.
cacheSolve: Ushbu funktsiya yuqoridagi makeCacheMatrix tomonidan qaytarilgan maxsus "matritsa" ning teskari qismini hisoblab chiqadi. Agar teskari hisoblangan bo'lsa (va matritsa o'zgarmagan bo'lsa), u holda keshlash keshidan teskari tomonni qaytarib olishi kerak.
Kvadrat matritsaning teskari tomonini hisoblash R.dagi yechish funktsiyasi bilan amalga oshirilishi mumkin, masalan, X kvadrat qaytariladigan matritsa bo'lsa, u holda (X) teskari natija beradi.

Ushbu topshiriq uchun ta'minlangan matritsa har doim o'zgaruvchan deb hisoblang.

Ushbu topshiriqni bajarish uchun siz quyidagilarni bajarishingiz kerak:

 O'zingizning hisob qaydnomangizda nusxasini yaratish uchun https://github.com/rdpeng/ProgrammingAssignment2 manzilida R stubli fayllarni o'z ichiga olgan GitHub omborini  oching.
Fayllarni o'zingizning shaxsiy kompyuteringizda tahrirlashingiz uchun o'zingizning GitHub omboringizni kompyuteringizga klonlang.
Git omboridagi R faylini tahrirlang va o'zingizning echimingizni ushbu faylga joylashtiring (iltimos, fayl nomini o'zgartirmang).
O'zingizning git omboringizga o'zingizning tugallangan R faylingizni kiriting va Git filialingizni o'zingizning hisobingiz ostidagi GitHub omboriga o'tkazing.
Kurseraga topshiriq uchun tugallangan R kodini o'z ichiga olgan GitHub omboringizga yuboring.
GitHub omboringiz uchun URL manzilini yuborishdan tashqari, sizga   fayllar versiyasini o'z ichiga olgan omborxona majburiyatini aniqlaydigan 40 ta belgidan iborat SHA-1 xashini (0-9 raqamlari qatori va af harflari qatori) kiritishingiz kerak bo'ladi. topshirmoqchiman. Buni GitHub-da quyidagilarni amalga oshirishingiz mumkin

Ushbu topshiriq uchun GitHub omboringiz veb-sahifasiga o'ting
"?? majburiyatlar "havolasi qaerda ?? bu sizning omboringizda bo'lgan majburiyatlar soni. Masalan, ushbu omborga jami 10 ta majburiyat kiritgan bo'lsangiz, havolada "10 ta majburiyat" yozilishi kerak.
Siz ushbu omborga qilgan majburiyatlaringiz ro'yxatini ko'rasiz. Eng so'nggi majburiyat eng yuqori qismida. Agar bu siz yubormoqchi bo'lgan fayllarning versiyasini ko'rsatadigan bo'lsa, shunchaki SHA-1 xeshi ustiga qo'yilganda paydo bo'lishi kerak bo'lgan "clipboardga nusxalash" tugmachasini bosing. Topshiriqni topshirganingizda ushbu SHA-1 xeshini kurs veb-saytiga joylashtiring. Agar siz eng so'nggi majburiyatdan foydalanishni xohlamasangiz, pastga tushing va kerakli topshiriqni toping va SHA-1 xashini nusxa oling.
Haqiqiy topshirish shunga o'xshash ko'rinishga ega bo'ladi (bu shunchaki  misol !)

1
