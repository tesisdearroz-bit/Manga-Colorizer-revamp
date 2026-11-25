# GitHub migration notes

This package is a cleaned copy of Manga-Colorizer Revamp prepared for uploading to a GitHub repository.

## Security
- The original `Backend/ssl/server.key` and `Backend/ssl/server.csr` were excluded. Do not commit private keys or API credentials.
- `Backend/ssl/server.crt` is retained, but it is a self-signed certificate from the source archive. For a public deployment, create a new certificate appropriate to your setup.
- `.gitignore` excludes private keys, local environments, caches, and generated output files.

## Model weights
- The included CycleGAN checkpoint is `Backend/networks/latest_net_G_A.pth`.
- The included ESRGAN checkpoint is `Backend/networks/RealESRGAN_x4plus_anime_6B.pt`.
- The included denoising checkpoint is `Backend/denoising/models/net_rgb.pth`.
- The README describes a separate download for `Backend/networks/generator.zip` for AlacGAN. That file was not present in the supplied archive and is ignored by Git.

## Upload
Create a repository on GitHub and upload the contents of the `Manga-Colorizer` folder (not the outer ZIP wrapper). Keep the repository private if you do not intend to publish the source and included model weights.
