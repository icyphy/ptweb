all: index.shtml committees.shtml cfp.shtml

index.shtml: header.html footer.html main
	cat header.html main footer.html > index.shtml

committees.shtml: header.html footer.html committees
	cat header.html committees footer.html > committees.shtml

cfp.shtml: header.html footer.html cfp
	cat header.html cfp footer.html > cfp.shtml

