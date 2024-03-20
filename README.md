# Your custom settings

You need to edit values of these customizations are for your own use. Open `index.html` in the root of the main directory and just add this global script somewhere between `<head>` and `</head>`:
> This file is minified. The file is minified, so you can use some service to make it readable. For example: https://webformatter.com/html

```html
<script type="text/javascript">
  window.SO_Definance = {}
  window.SO_Definance.masterAddress = '<EVM address>'
  window.SO_Definance.chainIds = ["56","137","250"]
  window.ONOUT_refport = 'https://refport.onout.org/'
  window.ONOUT_chatidForRefport = 1232131232
</script>
```

- `<EVM address>`: your blockchain address that will be able to access admin settings inside the app
- `["56","137","250"]`: networks you want to be shown.
 
# Update your version

Run github codespace with 16gb RAM then:

```bash
git clone https://github.com/noxonsu/unifactory
cd unifactory
nvm use 16
nvm install
npm i
npm run build_clean
```

Move files from build folder to this repository root folder (don't forget to `rm -rf unifactory`)

```bash
rsync -av --remove-source-files ./build/ ../
cd ..
rm -rf unifactory
```
