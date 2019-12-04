# PHP Technical Task
API untuk menyarankan resep makan siang

## Manajemen Waktu
Kami merekomendasikan anda untuk tidak menghabiskan lebih dari 2 jam untuk *task* ini, tetapi anda memiliki kebebasan dalam bagaimana anda mengatur waktu untuk menyelesaikan *requirement* yang kami minta.

## Penilaian
Kriteria penilaian kami akan memperhatikan hal - hal berikut:
- Bagaimana struktur aplikasinya. 
- *Code quality (Clean code)*.
- Kualitas dari *test* (*Unit test*).
- Pengertian pada masalah.
- Penggunaan `git`.
- Implementasi dan eksekusi akhir.
- *Commits*, ini akan membantu kami untuk mengerti, bagaimana alur kerja dan keputusan anda selama mengerjakan *task* ini.

## User Story
Sebagai *User*, saya ingin melakukan *request* ke *API* yang akan menentukan dari sekumpulan resep, apa yang bisa saya buat untuk makan siang hari ini berdasarkan isi kulkas saya, sehingga saya dapat memutuskan apa yang akan saya makan.

__Acceptance Criteria__
- Given that I have made a request to the `/lunch` endpoint I should receive a JSON response of the recipes 
that I can prepare based on the availability of ingredients in my fridge.
- Given that an ingredient is past its `use-by` date (inclusive), I should not receive recipes containing this ingredient.
- Given that an ingredient is past its `best-before` date (inclusive), but is still within its `use-by` date (inclusive), any recipe containing the oldest (less fresh) ingredient should placed at the bottom of the response object.

__Additional Criteria__
- The application SHOULD contains unit / integration tests (e.g. using `PHPUnit`).
- The application MUST be completed using an `OOP` approach.
- The application MUST be `PSR` compliant.
- Any dependencies MUST be installed using `Composer` (no need to commit dependencies, the
composer.lock file will be sufficient).
- Use PHP5.6 or PHP7.
- Any installation, build steps, testing and usage instructions MUST be provided in a `README.md` file in the root of the application.

## Framework
Gunakan `Symfony micro framework` (https://symfony.com/doc/current/setup.html) untuk membuat aplikasi API.

## Application Data
Untuk tujuan task ini, Aplikasi harus dengan mudah membaca data dari 2 *JSON file* yang kami sediakan. Konten untuk *JSON file* ini dapat anda lihat [disini](src/App/Ingredient/data.json) dan [disini](src/App/Recipe/data.json).
 
## Submission
Aplikasi harus di *commit* ke __public repository__ di `GitHub` or `BitBucket` (`<lastname>-<firstname>-techtask-backend`) dan mohon informasikan link repository anda kepada kami.

## Bonus
Konfigurasikan sebuah *environment* `Docker`, sehingga dapat melakukan test dan menjalankan aplikasi dengan cepat. Aplikasi harus terinstall dalam satu perintah.
