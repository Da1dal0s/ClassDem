# Logo Files

Please add the following logo image files to this directory:

1. **erc-eu.png** - The combined EU flag + ERC logo image
2. **ukri.png** - The UKRI logo image
3. **edinburgh.png** - The University of Edinburgh logo image

## How to Add Logos

### Via GitHub Web Interface:
1. Go to https://github.com/Da1dal0s/ClassDem
2. Navigate to `assets/images/logos/`
3. Click "Add file" → "Upload files"
4. Drag and drop the three PNG files
5. Commit the changes

### Via Git Command Line:
```bash
# Copy your logo files to this directory
cp /path/to/erc-eu.png assets/images/logos/
cp /path/to/ukri.png assets/images/logos/
cp /path/to/edinburgh.png assets/images/logos/

# Commit and push
git add assets/images/logos/*.png
git commit -m "Add footer logos"
git push
```

The logos will appear in the footer once uploaded.
