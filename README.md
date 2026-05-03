# VCD Mobil-O-Mat

## Requirements

Make these tools available in path:

- [GNU Make 4.x.x](https://www.gnu.org/software/make/)
- NodeJS, see version in [package.json](package.json)
- [Hugo](https://github.com/gohugoio/hugo)
- [qrtool](https://sorairolake.github.io/qrtool/book/index.html), only needed for `make qr-macos`
  - for macOS Homebrew: `brew install qrtool`

### Dependencies

```
npm install
```

## Commands

- Run local dev server
  ```
  make serve
  ```
- **macOS** Create qr code to scan with device in local network
  ```
  make qr-macos
  ```
  Combine it with `serve`
  ```
  make qr-macos serve
  ```

## Create your own VCD Mobil-O-Mat

- Adjust content in [hugo.yaml](hugo.yaml)
- Adjust [data/questions.yaml](data/questions.yaml)
- Adjust [content/datenschutz/\_index.md](content/datenschutz/_index.md)
- Deployment is done with Netcup. For different provider adjust [.github/workflows/build.yml](.github/workflows/build.yml)
  - Adjust `BASE_URL` to your domain in [.github/workflows/build.yml](.github/workflows/build.yml)
  - For Cloudflare Deployment see [cloudflare-deployment.md](docs/cloudflare-deployment.md)

## SVG Icons

Icons found here: https://leungwensen.github.io/svg-icon/#ionic
