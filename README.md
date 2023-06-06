# Get Liferay Info Action

Get current edition, major version and product name from your workspace.
Also fetch latest minor version and product name available for your current edition and major version.

## Basic Configuration

```yaml
steps:
  - uses: actions/checkout@v3
  - uses: lgdd/get-liferay-info-action@v1
    id: get-liferay-info
  - run: |
      echo ${{ steps.get-liferay-info.outputs.current-product-name }}
      echo ${{ steps.get-liferay-info.outputs.current-edition }}
      echo ${{ steps.get-liferay-info.outputs.current-major-version }}
      echo ${{ steps.get-liferay-info.outputs.current-minor-version }}
      echo ${{ steps.get-liferay-info.outputs.latest-product-name }}
      echo ${{ steps.get-liferay-info.outputs.latest-minor-version }}
      echo ${{ steps.get-liferay-info.outputs.latest-product-version-name }}
```

In this example we just print the available outputs from this action. Of course you can use those outputs as you want in your following steps.
Note that you can change the id value for the step using this action. If you do so, make sure to follow the following pattern: `steps.<step-id>.outputs.<output-name>`

## License

[MIT](LICENSE)
