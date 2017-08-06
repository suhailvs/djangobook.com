## Deployment

run **make html** on master branch, then checkout to `gh-pages` branch, then remove files excpet **_build** folder, then copy items in folder **_build/html** to root folder


**Rename folders:**

    _static --> static 
    _images --> images

**now rename every occurrence of `src="_images/` with `src="images/` and `href="_static/` with `href="static/`:**

    find ./ -type f -readable -writable -exec sed -i 's/src="_images/src="images/g' {} \;
    find ./ -type f -readable -writable -exec sed -i 's/href="_static/href="static/g' {} \;

**Checkout this readme file since it also changed on rename**

    git checkout -- README.md


now add and commit changes then push to github

	git push origin gh-pages