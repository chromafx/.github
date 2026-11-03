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
| **[chromafx](https://github.com/chromafx/chromafx)** | Library — BMP, PNG, JPEG, GIF + filters on .NET 10; opt-in `ChromaFx.PixelArt` |
| **[chromafx-site](https://github.com/chromafx/chromafx-site)** | Docs for [chromafx.net](https://chromafx.net) (Cloudflare Pages) |
| **[.github](https://github.com/chromafx/.github)** | Organization profile README |

### Why ChromaFx

- **Deploy anywhere** — fully managed codecs; nothing extra for Docker/Lambda multi-arch
- **Explicit API** — `Mutate` / `Clone`, typed encoders, public `ImageFormats` registry
- **Lean stack** — no third-party NuGet dependencies on the hot path
- **Pixel art (opt-in)** — Scale2x / Scale3x / Hq2x–4x / CleanEdge / Eagle / SaI and `RotateSprite` / `CleanEdgeRotate` via `ChromaFx.PixelArt`

Current NuGet line is **0.6.0** (tag-only releases; 0.x may still change before 1.0):

```bash
dotnet add package ChromaFx
# optional pixel-art upscaling / rotation:
dotnet add package ChromaFx.PixelArt
```

```csharp
Image.Load("input.png")
    .Mutate(ctx => ctx.Resize(800, 600).Brightness(0.1f))
    .Save("output.jpg", new JpegEncoder { Quality = 85 });
```

### Links

- Site: [chromafx.net](https://chromafx.net)
- Site source: [chromafx/chromafx-site](https://github.com/chromafx/chromafx-site)
- Packages: [ChromaFx](https://www.nuget.org/packages/ChromaFx/) · [ChromaFx.PixelArt](https://www.nuget.org/packages/ChromaFx.PixelArt/)
- License: Apache 2.0

Fork of [Structure.Sketching](https://github.com/JaCraig/Structure.Sketching) by JaCraig. Maintained by Ho Tzin Mein.
