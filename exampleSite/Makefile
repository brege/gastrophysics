.PHONY: cv build serve clean

cv:
	hugo --quiet
	sed --quiet '1p; 2,/^---$$/p' content/cv/index.md > /tmp/gastrophysics-example-cv.md
	printf '\n' >> /tmp/gastrophysics-example-cv.md
	cat public/cv/index.md >> /tmp/gastrophysics-example-cv.md
	cmp --silent /tmp/gastrophysics-example-cv.md content/cv/index.md || cp /tmp/gastrophysics-example-cv.md content/cv/index.md

build: cv
	hugo

serve: cv
	hugo server

clean:
	rm -r public/ resources/_gen/
