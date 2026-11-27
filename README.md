# Foveal-Games

Le catalogue des patchs de jeux pour Foveal PC : pour chaque jeu, la dernière version de son patch et le post Patreon où la télécharger.
Foveal le lit pour signaler, dans la Fiche du jeu, qu'un nouveau patch est disponible. Ce dépôt ne contient aucun patch, aucun programme : seulement `catalog.json` et sa signature.

The game patch catalog for Foveal PC: for each game, its patch's latest version and the Patreon post to download it from.
Foveal reads it to show, on the game's sheet, that a new patch is out. This repository holds no patch and no program: only `catalog.json` and its signature.

## Format

```json
{
  "format": 1,
  "updated": "2026-11-27T10:00:00Z",
  "games": [
    {
      "exe": "game.exe",
      "title": "Game",
      "patch": { "version": "1.2", "page": "https://www.patreon.com/posts/...", "sha256": "…", "size": 123456, "date": "2026-11-27", "notes": "" }
    }
  ]
}
```

`catalog.json.sig` : signature ECDSA P-256 (SHA-256, r‖s en base64) des octets exacts de `catalog.json`. Foveal ignore un catalogue dont la signature ne correspond pas à sa clé publique.

`catalog.json.sig`: an ECDSA P-256 signature (SHA-256, r‖s in base64) of the exact bytes of `catalog.json`. Foveal ignores a catalog whose signature does not match its public key.
