# b2-download-action
[![Build Container Image](https://github.com/sksat/b2-download-action/actions/workflows/build-image.yml/badge.svg)](https://github.com/sksat/b2-download-action/actions/workflows/build-image.yml)
[![test Action](https://github.com/sksat/b2-download-action/actions/workflows/test-action.yml/badge.svg)](https://github.com/sksat/b2-download-action/actions/workflows/test-action.yml)

GitHub Action for download file from Backblaze B2

Example workflow
```yaml
jobs:
  download-b2:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2

      - uses: sksat/b2-download-action@main
        with:
          key_id: ${{ secrets.B2_KEY_ID }}
          key: ${{ secrets.B2_KEY }}
          bucket: ${{ secrets.B2_BUCKET }}
          src: hoge.txt
          dest: hoge.txt
```
