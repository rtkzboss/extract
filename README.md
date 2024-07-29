# extract
### :biohazard: Experimental
Uses dark magic to generate cooked packages from I/O store containers for read-only use in the editor.
- Example usage: `extract --epic -o C:\path\to\CrimeBoss -a /Game/00_Main/Characters/_Mutable/MutableGeneratorImages/T_Wiz_UniqueCharPhoto_0 -a /Game/00_Main/Core/AI/Spawning/BP_CivilianSpawnPoint --and-deps`
- See https://docs.unrealengine.com/4.27/en-US/WorkingWithContent/CookedContent/ for information on how to use cooked packages in the editor.

## Usage
```
Generate assets from CrimeBoss I/O store containers

Usage: extract.exe [OPTIONS] --game-dir <GAME_DIR> --out-dir <OUT_DIR>

Options:
      --store-dir <STORE_DIR>
          Path to the I/O store directory (e.g. 'C:\Program Files\Epic Games\CrimeBossRC\CrimeBoss\Content\Paks')
  -g, --game-dir <GAME_DIR>
          Path to the game directory (e.g. 'C:\Program Files\Epic Games\CrimeBossRC')
      --epic
          Convenience for --game-dir 'C:\Program Files\Epic Games\CrimeBossRC'
      --steam
          Convenience for --game-dir 'C:\Program Files (x86)\Steam\steamapps\common\CrimeBossRockayCity'
  -o, --out-dir <OUT_DIR>
          Write non-engine assets to the given directory
      --engine-out-dir <ENGINE_OUT_DIR>
          Write engine assets to the given directory
      --dry-run
          Don't generate any files and print what would be done
  -a, --asset <ASSETS>
          Extract the packages at the given paths (e.g. '/Game/CrimeBossMeta/Resources/DA_MetaData')
      --asset-list <ASSET_LISTS>
          Read --asset entries from the lines of the given file
      --asset-dir <ASSET_DIRS>
          Extract all packages in the given directory or its subdirectories (e.g. '/Game/CrimeBossMeta/Resources/Curves')
      --asset-pattern <ASSET_PATTERNS>
          Extract all packages with names that contain the given substring
      --asset-parent <ASSET_SUPERS>
          Extract all packages containing objects that inherit from the given base class (e.g. '/Script/GameplayAbilities.GameplayEffect')
      --asset-parent-list <ASSET_SUPER_LISTS>
          Read --asset-parent entries from the lines of the given file
  -c, --asset-class <ASSET_PARENTS>
          Extract all packages containing objects of the given class or its children (e.g. '/Script/Engine.Texture2D')
      --asset-class-list <ASSET_PARENT_LISTS>
          Read --asset-class entries from the lines of the given file
      --asset-class-exact <ASSET_CLASSES>
          Extract all packages containing objects of the given class and *not* its children (e.g. '/Script/Engine.BlueprintGeneratedClass')
      --exclude-class <EXCLUDE_PARENTS>
          Refuse to extract packages containing objects of the given class or its children
      --exclude-class-list <EXCLUDE_PARENT_LISTS>
          Read --exclude-class entries from the lines of the given file
      --and-deps
          Also extract packages' recursive dependencies
      --and-soft-deps
          Also extract packages' recursive dependencies, including all soft references
      --and-soft-deps-shallow
          Also extract packages' recursive dependencies, including direct soft references
  -v, --verbose...
          Show more information
      --stdout <STDOUT>
          [possible values: package-names, file-names]
      --concurrent-rewrites <CONCURRENT_REWRITES>
          Only generate the given number of packages at once [default: 256]
      --concurrent-imports <CONCURRENT_IMPORTS>
          Only preload the given number of packages at once [default: 4096]
      --project-dir-name <PROJECT_DIR_NAME>
          The game project directory name [default: CrimeBoss]
      --no-default-script-data
          Don't load the embedded script object metadata
      --script-data <SCRIPT_DATA>
          Read additional script object metadata from the given file
  -h, --help
          Print help
  -V, --version
          Print version
```
