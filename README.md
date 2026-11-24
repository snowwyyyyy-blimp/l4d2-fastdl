# L4D2 FastDL

FastDL files for the `Driveable Vehicles` SourceMod plugin on Left 4 Dead 2.

Folder layout mirrors the server install so Cloudflare Pages can serve files directly:

```
left4dead2/
  models/
    buggy.mdl / .vvd / .phy / .dx80.vtx / .dx90.vtx / .sw.vtx
    airboat.mdl / .vvd / .phy / .dx80.vtx / .dx90.vtx / .sw.vtx
  scripts/
    game_sounds_vehicles.txt
    vehicles/
      jeep_test.txt
      airboat.txt
```

## Cloudflare Pages

- Build command: *(none)*
- Build output directory: `/`
- Root branch: `main`

## Server

Point `sv_downloadurl` at the Pages URL, e.g.:

```
sv_downloadurl "https://l4d2-fastdl.pages.dev"
```

The server will then request files such as:

```
https://l4d2-fastdl.pages.dev/left4dead2/models/buggy.mdl
```

## Credits

Vehicle models and scripts originate from Half-Life 2 (Valve) and were sourced from
the public [Pinsplash/halflife2chaos](https://github.com/Pinsplash/halflife2chaos)
repository. No assets are redistributed for commercial use.
