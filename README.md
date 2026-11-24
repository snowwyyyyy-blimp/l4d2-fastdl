# L4D2 FastDL

FastDL files for the `Driveable Vehicles` SourceMod plugin on Left 4 Dead 2.

Folder layout mirrors the server install so Cloudflare Pages can serve files directly.
L4D2's FastDL client requests `.bz2`-compressed copies, so each asset exists both
uncompressed and as `<filename>.bz2`:

```
left4dead2/
  models/
    buggy.mdl / .vvd / .phy / .dx80.vtx / .dx90.vtx / .sw.vtx
    airboat.mdl / .vvd / .phy / .dx80.vtx / .dx90.vtx / .sw.vtx
  materials/models/
    buggy/ammo_box.vmt + .vtf, buggy001.vmt + .vtf
    airboat/airboat001.vmt + .vtf, airboat_blur02.vmt + .vtf
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
[Pinsplash/halflife2chaos](https://github.com/Pinsplash/halflife2chaos).
Materials were sourced from
[bouletmarc/hl2_ep2_content](https://github.com/bouletmarc/hl2_ep2_content).
No assets are redistributed for commercial use.
