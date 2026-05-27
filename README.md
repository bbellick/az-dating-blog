# Azərbaycanda Tanışlıq — Sayt Rəhbəri

Bu fayl saytı necə idarə etmək lazım olduğunu izah edir.

---

## Yeni məqalə əlavə etmək (Obsidian ilə)

### 1. Doğru qovluğu seç

| Məqalə növü | Qovluq |
|-------------|--------|
| Sayt rəyi (Tinder, Badoo...) | `content/obzor/` |
| Müqayisə cədvəli | `content/muqayise/` |
| Təhlükəsizlik məqaləsi | `content/tehlukesizlik/` |

### 2. Yeni fayl yarat

Obsidian-da seçilmiş qovluğa yeni `.md` faylı yarat.  
Ad ingilis hərfləri ilə olsun, boşluqsuz: `yeni-meqale.md`

### 3. Faylın başına bu məlumatı əlavə et (frontmatter)

```
---
title: "Məqalənin başlığı"
description: "Qısa açıqlama (Google-da görünəcək)"
date: 2026-05-26
slug: "url-de-gorunecek-ad"
tags: ["etiket1", "etiket2"]
showToc: true
---

Burada mətn yazırsınız...
```

### 4. Publish et

Obsidian Git plaginini açın:  
`Ctrl + P` → `Git: Commit all changes and push`

Netlify 30 saniyə ərzində saytı yeniləyəcək.

---

## Şablon — Sayt Rəyi

```markdown
---
title: "SAYT ADI Azərbaycanda: Dürüst Rəy"
description: "SAYT ADI-nin Azərbaycanda istifadəsi haqqında rəy."
date: 2026-05-26
slug: "sayt-adi"
tags: ["sayt-adi", "tanışlıq", "rəy"]
showToc: true
---

## SAYT ADI nədir?

[Qısa giriş]

## Azərbaycanda vəziyyəti

| Göstərici | Qiymət |
|-----------|--------|
| İstifadəçi sayı | Yüksək / Orta / Aşağı |
| Pulsuz funksiyalar | ★★★☆☆ |
| Ödənişli tələlər | ★★★☆☆ |
| Saxta profillər | ★★☆☆☆ |
| Ümumi qiymət | **X/10** |

## Üstünlüklər

- ...

## Çatışmazlıqlar

- ...

## Nəticə

[Tövsiyə]
```

---

## Obsidian Git quraşdırması (bir dəfəlik)

1. Obsidian → **Settings** → **Community plugins** → Browse
2. "**Obsidian Git**" axtarın → Install → Enable
3. Settings → Obsidian Git:
   - `Vault backup interval (minutes)`: **10**
   - `Auto push after commit`: **açıq**
4. `Ctrl + P` → `Git: Open source control view` — hər şeyin işlədiyini yoxlayın

---

## GitHub-a ilk yükləmə

```bash
# Terminal-də bu əmrləri icra et:
cd "C:\Users\mbidz\Desktop\2026\Ar_Project"
git remote add origin https://github.com/SENIN_ADIN/az-dating-blog.git
git add .
git commit -m "ilk versiya"
git push -u origin main
```

---

## Domeni dəyişmək

Domeni satın aldıqdan sonra `hugo.toml` faylının ilk sətirini dəyiş:

```toml
baseURL = "https://SENIN_DOMENIN.com/"
```

---

## Yerli ön izləmə

```bash
hugo server
```

Brauzer: `http://localhost:1313`

---

## Faydalı linklər

- [Netlify dashboard](https://app.netlify.com)
- [GitHub repo](https://github.com)
- [Namecheap domain](https://namecheap.com)
- [Hugo sənədləri](https://gohugo.io/documentation/)
