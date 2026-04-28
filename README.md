# eCommerce Project - Movie Store

ASP.NET Core MVC ile geliştirilmiş film satış ve yönetim uygulaması. Filmler, aktörler, yapımcılar ve sinema salonları üzerinde CRUD işlemleri yapılabilir; kullanıcılar filmleri sepete ekleyip satın alabilir.

## Teknolojiler

- ASP.NET Core MVC (.NET 8)
- Entity Framework Core (Code First + Migrations)
- SQL Server
- Razor Views (cshtml)

## Proje Yapısı

```
ecommerceProject/
├── Controllers/
│   ├── ActorsController.cs
│   ├── CinemaController.cs
│   ├── MoviesController.cs
│   └── ProducersController.cs
├── Data/
│   ├── Base/            # Generic repository pattern
│   ├── Enums/
│   ├── Services/        # İş mantığı servisleri
│   ├── AppDbContext.cs
│   └── AppDbInitializer.cs
├── Migrations/
├── Models/
│   ├── Actor.cs
│   ├── Actor_Movie.cs   # Many-to-many ilişki
│   ├── Cinema.cs
│   ├── Movie.cs
│   └── Producer.cs
├── Views/
│   ├── Actors/
│   ├── Cinema/
│   ├── Movies/
│   ├── Producers/
│   └── Shared/
├── wwwroot/
└── appsettings.json
```

## Özellikler

- Film, aktör, yapımcı ve sinema salonu CRUD işlemleri
- Sepete ekleme ve satın alma (Add to Cart)
- Generic Repository Pattern ile veri erişim katmanı
- Entity Framework Code First ve migration desteği
- Seed data ile başlangıç verileri
- Film-Aktör many-to-many ilişki yönetimi

## Kurulum

1. Projeyi klonlayın:
   ```
   git clone https://github.com/<kullanici>/ecommerceProject.git
   ```
2. Visual Studio 2022 ile `ecommerceProject.sln` dosyasını açın.
3. `appsettings.json` içindeki connection string'i kendi SQL Server'ınıza göre düzenleyin.
4. Package Manager Console'da migration'ları uygulayın:
   ```
   Update-Database
   ```
5. Projeyi çalıştırın (F5).
