PDFLATEX = pdflatex

DIRS = 	overview \
	introduction \
	trees \
	complexity \
	higher





WWW =  ~/afs/public_html/courses/id1019/lectures

TRACER = ppm.erl test1.ppm vector.erl camera.erl objects.erl tracer.erl test.erl world.erl lights.erl tracer1.erl tracer2.erl tracer3.erl test.erl

all:
	echo $(DIRS)
	for d in $(DIRS); do  echo ./$$d; cd $$d && make && cd ..; \
        done
link:
	for d in $(DIRS); do\
             cd $$d;\
             ln -s ../include/Makefile .; \
	     ln -s ../include/handout.tex .; \
             cd ../;\
        done

install: 
	for d in $(DIRS); \
             do rsync -u ./$$d/handout-nup.pdf $(WWW)/$$d.pdf;\
        done


itracer : 
	for d in $(TRACER); \
	    do cp ./tracer/$$d $(WWW)/tracer/$$d;\
        done


clean : 
	for d in $(DIRS); do cd ./$$d && make clean && cd ..; \
        done

realclean : 
	for d in $(DIRS); do cd ./$$d && make realclean && cd ..; \
        done


