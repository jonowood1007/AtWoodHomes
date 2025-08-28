I can't generate PNG/ICO images reliably without an image processing tool in this environment, but here are PowerShell commands you can run locally (requires ImageMagick `magick` command) to generate the favicons from `assets/logo.jpg`.

Commands (PowerShell):

# create 16x16 and 32x32 PNG
magick assets/logo.jpg -resize 32x32 assets/favicon-32x32.png
magick assets/logo.jpg -resize 16x16 assets/favicon-16x16.png

# create multi-resolution ICO (contains 16x16 and 32x32)
magick assets/favicon-16x16.png assets/favicon-32x32.png assets/favicon.ico

# quick test: open index.html in browser and do a hard refresh (Ctrl+F5)

If you want, I can add those generated files to the repo if you run the commands locally and upload them, or paste base64 data and I can create the files here.
