# CWF-Images

Copying CWF images to /tmp/cwf-images
```bash
cd images //where cwf docker images are saved
sudo vi script.sh
```

Insert this content to script.sh

for IMAGES in `ls -a1 *.gz`
do
  gzip -d $IMAGES
done
mkdir -p /tmp/cwf-images
cp cwf_*.tar /tmp/cwf-images

After this save and exit

Now, run created script
```bash
sudo chmod 755 script.sh
./script.sh
```
