<h3 align="center">Welcome to my guide on making VRChat Mods</h3>

---

## 📝 Table of Contents

- [About](#about)
- [Requirements](#requirements)
- [SetUp](#Setup)
- [MelonLoader setup](#melonloaderstart)
- [MelonLoader Logging](#melonloaderlogging)
- [Authors](#authors)
- [Copyright and credit](#Copyright)

## 🧐 About <a name = "about"></a>

This is my guide on how to make VRChat Mods for MelonLoader. I decided to make this because I couldn't find any guides or anything on making or even getting started on making mods. I will go into details about where to start and what is needed to be able to start developing mods.

## Requirements <a name = "requirements"></a>

| Requirements  |
| ------------- |
| VRChat with melonloader installed  |
| Visual Studio with C# installed |

| Dlls  |
| ------------- |
| MelonLoader.dll |
| UIExpansionKit.dll |

## SetUp <a name = "Setup"></a>

First of all you'll need to create a 'Class Library (.NET Framework)' and set the framework to '.NET Framework 4.7.2'. Once you've created the project you will need to add MelonLoader.dll and UIExpansionKit.dll as References, After you've done that you will then need to add it to the top of your file by doing 'using MelonLoader;' and 'using UIExpansionKit.API;'

## MelonLoader setup <a name = "melonloaderstart"></a>

Once you've got the References setup you can start setting up your project for MelonLoader to load, You want start with setting the build info this can be done by doing

```
public static class BuildInfo
    {
        public const string Name = "Mod Name"; // (MUST BE SET)
        public const string Description = "Mod Description"; // (Set as null if none)
        public const string Author = "Mod Author"; // (MUST BE SET)
        public const string Company = "Company that made the mod"; // (Set as null if none)
        public const string Version = "Mod Version"; // (MUST BE SET)
        public const string DownloadLink = "Mod download link"; // (Set as null if none)
    }
```

After you've added the buildinfo now you will need to add at the end of 'Public class class1' you will want to add a space then put ': MelonMod'

## MelonLoader Logging <a name = "melonloaderlogging"></a>

Now that your project is set up I will now show you how to print text into the MelonLoader Console, This can be useful for checking for errors and now it'll be used for testing to see if the project is working correctly.

```
Public override void OnApplicationStart()
{
  MelonLogger.Msg("Hello VRChat");
}
```


## ✍️ Authors <a name = "authors"></a>

- [@Mattyelele](https://github.com/Mattyelele) - Creator
- [@Jackelele](https://github.com/Jackelele) - README.md layout

## Copyright and credit <a name = "Copyright"></a>

- [@TheMaskedMan00](https://github.com/TheMaskedMan00/MaskedShitMod) - they're MaskedShitMod project helped me figure out where to start.
