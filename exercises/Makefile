DIRS =	huffman \
	introduction \
	lambda \
	mandel \
	morse \
	twothree



WWW =  ~/afs/public_html/courses/id1019/seminars


all:
	echo $(DIRS)
	for d in $(DIRS); do  echo ./$$d; cd $$d && make && cd ..; \
        done

install: 
	for d in $(DIRS); \
             do rsync -u ./$$d/assignment.pdf $(WWW)/$$d/$$d.pdf;\
        done


clean : 
	for d in $(DIRS); do cd ./$$d && make clean && cd ..; \
        done

realclean : 
	for d in $(DIRS); do cd ./$$d && make realclean && cd ..; \
        done


