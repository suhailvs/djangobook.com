## Deployment

**Rename folders:**

    _static --> static 
    _images --> images

**now rename every occurrence of `src="_images/` with `src="images/`:**

    find ./ -type f -readable -writable -exec sed -i 's/src="_images/src="images/g' {} \;

**Checkout this readme file since it also changed on rename**

    git checkout -- README.md