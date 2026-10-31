<p align="center">
  <img src="https://raw.githubusercontent.com/chromafx/chromafx/master/assets/banner.png" alt="ChromaFx" width="720" />
</p>

<h1 align="center">ChromaFx</h1>

<p align="center">
  <strong>Modern .NET image processing — pure managed C#, no native codec DLLs.</strong>
</p>

<p align="center">
  <a href="https://chromafx.net">chromafx.net</a> ·
  <a href="https://www.nuget.org/packages/ChromaFx/">NuGet</a> ·
  <a href="https://github.com/chromafx/chromafx">Library</a> ·
  <a href="https://github.com/chromafx/chromafx-site">Docs</a>
</p>

---

### What we build

| Repo | What it is |
|------|------------|
| **[chromafx](https://github.com/chromafx/chromafx)** | Core library — BMP, PNG, JPEG, GIF decode/encode + filters on .NET 10 |
| **[chromafx-site](https://github.com/chromafx/chromafx-site)** | Documentation site for [chromafx.net](https://chromafx.net) |
| **[.github](https://github.com/chromafx/.github)** | Organization profile README |

### Why ChromaFx

- **Deploy anywhere** — fully managed codecs; nothing to ship for Docker/Lambda multi-arch
- **Explicit API** — `Mutate` / `Clone`, typed encoders, public `ImageFormats` registry
- **Lean stack** — no third-party NuGet dependencies on the hot path

```bash
dotnet add package ChromaFx
```

```csharp
Image.Load("input.png")
    .Mutate(ctx => ctx.Resize(800, 600).Brightness(0.1f))
    .Save("output.jpg", new JpegEncoder { Quality = 85 });
```

### Links

- Site: [chromafx.net](https://chromafx.net)
- Site source: [chromafx/chromafx-site](https://github.com/chromafx/chromafx-site)
- Packages: [ChromaFx on NuGet](https://www.nuget.org/packages/ChromaFx/)
- License: Apache 2.0

Fork of [Structure.Sketching](https://github.com/JaCraig/Structure.Sketching) by JaCraig. Maintained by Ho Tzin Mein.
