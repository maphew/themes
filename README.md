# acrylamid-themes pages


Demo and test pages for [acrylamid-themes](https://github.com/posativ/themes).

## Recipe for building

### Initialize GH pages
Adapted from instructions at https://help.github.com/articles/creating-project-pages-manually

	git clone https://github.com/posativ/themes.git acrylic-pages
	cd acrylic-pages
	git rm -rf .

	cd ..
	acrylamid init acrylamid-staging
	cd acrylamid-staging
	vim conf.py

add following:

	#THEME = 'themes/default'
	#WWW_ROOT = 'http://posativ.github.com/themes/default'
	THEME = 'themes/bootstrap'
	WWW_ROOT = 'http://posativ.github.com/themes/bootstrap'

[Un]comment and compile as needed:

	acrylamid compile
	move output\themes\bootstrap ..\acrylic-pages\bootstrap

And finally commit changes, 
and test by visting [http://posativ.github.com/themes/](http://posativ.github.com/themes/)
