# Theme Files for EZ-Flash Omega Definitive Edition

This guide explains how to use, edit, and install custom themes (`.skn` files) for the EZ-Flash Omega Definitive Edition (Omega DE). These themes customize the UI.

---

## Directory Structure

Place your themes inside the following structure on the microSD card:

```
/THEMES/
  YourThemeName/
    theme.skn
    icon.bmp
    bg.bmp
    font.bmp
```

**Note:** Some systems are case-sensitive. Match casing exactly if your theme doesn't appear.

---

## Required Files

| File        | Description                  | Format        | Required |
|-------------|------------------------------|----------------|----------|
| `theme.skn` | Main skin configuration      | Binary `.skn`  | Yes      |
| `bg.bmp`    | Background image             | 16-bit BMP     | Yes      |
| `font.bmp`  | Bitmap font sheet            | 16-bit BMP     | Yes      |
| `icon.bmp`  | Top-left UI icon             | 16-bit BMP     | If used  |

---

## Tools for Editing

- [EZ-Flash Theme Editor](https://www.ezflash.cn/themeEditor/)
- [GIMP](https://www.gimp.org/) or Photoshop for editing BMPs
- [IrfanView](https://www.irfanview.com/) for quick conversion

Save images in **16-bit RGB565** format. Most editors default to 24-bit-these will not work.

---

## Tips and Best Practices

- Keep image dimensions consistent with the default kernel resolution
- Use contrasting colors between font and background for readability
- Avoid using spaces or special characters in file or folder names
- Test theme visibility with long and short ROM names

---

## Advanced Customization

- `.skn` files may include layout, transparency, cursor offsets, and more
- Some third-party tools allow unpacking `.skn` files for direct edits
- Themed kernels apply global styles alongside your theme assets

---

## Where to Find Themes

- [EZ-Flash Forum Skins](https://bbs.ezflash.cn/forum-52-1.html)
- [GBATemp Skins Thread](https://gbatemp.net/threads/ez-flash-omega-definitive-edition-skin-thread.574149/)
- Reddit and Discord communities may share custom themes

---

## Related Guides

- [Theme Creation Tutorial](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Tutorials/Creating_Themes.md)
