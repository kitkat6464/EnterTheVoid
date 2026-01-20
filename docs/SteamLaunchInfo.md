<div align="center">
Steam Game Launch Setting's
</div>

> [!TIP]
> Use PC Game Wiki To Double Check FSR 4 Support, Also Use SANE Launch Parameters From ProtonDB.

## Non FS4 Game's: 

```shell
scb -O DP-2 -- %command%
```

## FSR4 Game's: (HL, Horizon, Spiderman, Stalker, Clair, Rivals, Rachet, Black Myth, Ghost of)

```shell
PROTON_FSR4_UPGRADE=1 scb -O DP-2 -- %command%
```

## Other Game's:

```shell
GoW: Rag: SteamDeck=1 PROTON_FSR4_UPGRADE=1 scb -O DP-2 -- %command%
```

```shell
Cyberpunk: PROTON_FSR4_UPGRADE=1 scb -O DP-2 -- %command% --launcher-skip
```

```shell
Witcher 2: eval $( echo "scb -O DP-2 -- %command%" | sed "s/Launcher.exe'.*/bin\/witcher2.exe'/")
```

```shell
Witcher 3: scb -O DP-2 -- %command% --launcher-skip
```
