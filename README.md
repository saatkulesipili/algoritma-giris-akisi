# Kullanıcı Giriş Akışı — Algoritma Diyagramı

## Projenin Amacı
Bu projenin amacı, bir web uygulamasındaki kullanıcı giriş sürecini algoritma ve akış diyagramı kullanarak modellemektir.

Algoritmada kullanıcının e-posta ve şifre bilgilerinin kontrol edilmesi, yanlış girişlerde başarısız deneme sayısının artırılması ve üç başarısız deneme sonucunda hesabın kilitlenmesi gibi durumlar gösterilmektedir. Bu çalışma ile koşul yapıları, sayaç kullanımı ve akış diyagramı sembollerinin doğru şekilde kullanılması amaçlanmıştır.

## İş Kuralları
- Hesabın kilitli olup olmadığı kontrol edilir.
- E-posta veya şifre alanlarından biri boş bırakılırsa uyarı gösterilir.
- Boş alan durumunda başarısız giriş sayısı artırılmaz.
- E-posta ve şifre doğruysa başarılı giriş sonucu gösterilir.
- E-posta veya şifre yanlış ise başarısız giriş sayısı 1 artırılır.
- Üç başarısız denemede hesap kilitlenir.
- Hesap kilitliyse kullanıcı giriş yapamaz.

## Akış Diyagramı

<img width="3309" height="4672" alt="Kullanıcı-Giriş-Algoritmas-Akış-Diyagramı" src="https://github.com/user-attachments/assets/82d22cd1-df32-4871-b04f-41f0c2594780" />


## Test Senaryoları
| Senaryo | Beklenen sonuç |

## Test Senaryoları
| Senaryo | Beklenen sonuç |
|---|---|
| Hesap kilitli | Giriş engellenir |
| E-posta veya şifre boş | Uyarı gösterilir, sayaç artmaz |
| Bilgiler doğru | Başarılı giriş |
| İlk yanlış giriş | Sayaç 1 artırılır |
| İkinci yanlış giriş | Sayaç 1 artırılır |
| Üçüncü yanlış deneme | Hesap kilitlenir ve giriş engellenir |

## Tasarım Kararları
Algoritmanın başlangıcında başarısız giriş sayacı 0 olarak kabul edilmiştir.

İlk olarak hesabın kilitli olup olmadığı kontrol edilir. Hesap kilitliyse kullanıcıya girişin engellendiği bilgisi gösterilir.

Hesap kilitli değilse e-posta ve şifre alanlarının boş olup olmadığı kontrol edilir. Alanlardan herhangi biri boşsa kullanıcıya uyarı gösterilir ve başarısız giriş sayısı artırılmaz.

Alanlar doluysa girilen e-posta ve şifre bilgileri kontrol edilir. Bilgiler doğruysa başarılı giriş işlemi gerçekleştirilir. Bilgiler yanlışsa başarısız giriş sayacı 1 artırılır.

Sayaç değeri 3'e ulaştığında hesap kilitlenir. Böylece kullanıcı üç başarısız girişten sonra tekrar giriş yapamaz.

## Öğrenci Bilgisi
- Ad Soyad: M.Hakan Gök
- Ödev: Algoritma Tasarımı ve Akış Diyagramı
