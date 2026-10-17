# Kurulum Rehberi (Türkçe)

Bu klasörde senin GitHub profilin için hazır bir README var. Çalışması için yapman gerekenler aşağıda.

## 1. Profil README repo'sunu oluştur

GitHub profil README'i **kullanıcı adınla aynı isimdeki** repo'da görünür.

1. GitHub'da **yeni repo** oluştur: adı tam olarak `EfeKaraer` olsun (büyük/küçük harf önemli).
2. Repo'yu **Public** yap ve "Add a README file" seçeneğini **işaretleme**.
3. Bu klasördeki dosyaları o repo'ya yükle.

### Yükleme (git ile)

```bash
cd "C:\Users\Efe Karaer\Desktop\readme"
git init
git add .
git commit -m "Add profile README"
git branch -M main
git remote add origin https://github.com/EfeKaraer/EfeKaraer.git
git push -u origin main
```

> `.github/workflows/snake.yml` dosyası gizli `.github` klasöründe. `git add .` bunu da ekler, ayrıca bir şey yapmana gerek yok.

### Yükleme (tarayıcıdan, git olmadan)

1. Repo sayfasında **Add file → Upload files**.
2. `README.md` dosyasını sürükle-bırak.
3. Yılan animasyonu için: **Add file → Create new file**, dosya adına `.github/workflows/snake.yml` yaz ve `snake.yml` içeriğini yapıştır.

## 2. Yılan (snake) animasyonunu çalıştır

README'deki yılan animasyonu, repo'ya eklenen GitHub Action ile üretilir.

1. Repo → **Actions** sekmesine git.
2. Sol taraftan **Generate Snake** workflow'unu seç.
3. **Run workflow** butonuna bas (ilk çalıştırma manuel).
4. Yaklaşık 1 dakika sonra `output` adında bir branch oluşur ve README'deki yılan belirir.
5. Bundan sonra her gün gece 00:00'da otomatik güncellenir.

**Önemli:** Action'ın repo'ya yazabilmesi için izin gerekir:
Repo → **Settings → Actions → General → Workflow permissions** → **Read and write permissions** seçeneğini işaretle ve kaydet.

Yılan ilk çalışmadan önce README'de kırık resim olarak görünür, bu normaldir.

## 3. İçeriği kişiselleştir

| Ne değiştirmek istiyorsun? | Nerede? |
|---|---|
| Yazı animasyonundaki yazılar | README'deki `readme-typing-svg` linkindeki `lines=...` kısmı (`+` ile ayrılır, boşluklar `+`) |
| Üst banner yazısı/rengi | En üstteki `capsule-render` linki (`text=`, `color=0:...,100:...`) |
| Teknoloji ikonları | `skillicons.dev/icons?i=ts,js,react...` — isimler [skillicons.dev](https://skillicons.dev) sitesinde |
| Renk teması | Tüm kartlardaki `theme=tokyonight` → `radical`, `dracula`, `github_dark`, `nord`, `catppuccin_mocha` |
| Öne çıkan projeler | `Featured Projects` bölümündeki `repo=` kısımları — istediğin 4 repoyu koy |
| Konum / öğrenci rozetleri | `img.shields.io` ile başlayan satırlar |

### Renk temasını tek seferde değiştirmek

`README.md` içinde `tokyonight` kelimesini `dracula` (veya başka bir tema) ile değiştir, tüm kartlar birlikte değişir.

## 4. Şu an kapalı olan servisler

Aşağıdaki iki popüler servis şu anda herkese açık sunucularında yanıt vermiyor (402 hatası), bu yüzden README'ye eklemedim:

- `github-profile-trophy` (kupa kartları)
- `github-readme-activity-graph` (katkı grafiği)

İleride düzelirse şu satırları `GitHub Stats` bölümüne ekleyebilirsin:

```html
<img src="https://github-profile-trophy.vercel.app/?username=EfeKaraer&theme=tokyonight&no-frame=true&column=7" />
<img src="https://github-readme-activity-graph.vercel.app/graph?username=EfeKaraer&theme=tokyonight&hide_border=true" />
```

Kendi sunucuna kurmak hakkında bilgi isteyen olursa ikisi de açık kaynak: [github-profile-trophy](https://github.com/ryo-ma/github-profile-trophy), [github-readme-activity-graph](https://github.com/Ashutosh00710/github-readme-activity-graph).

## 5. Kontrol listesi

- [ ] `EfeKaraer` adında public repo oluşturuldu
- [ ] `README.md` yüklendi, profil sayfasında görünüyor
- [ ] `Settings → Actions → General → Workflow permissions` = Read and write
- [ ] `Generate Snake` workflow'u manuel çalıştırıldı
- [ ] `output` branch oluştu, yılan görünüyor
- [ ] İstatistik kartlarında senin verilerin çıkıyor (kullanıcı adı doğru yazılmış)
