# ECCSI-SAKKE
Crypto library and demonstration code for ECCSI/ SAKKE (RFC 6507 and 6508)

Note! If you are viewing this page on the github web page, there is a wiki
link on the right hand side of the project screen that provides more details.

Overview
--------
    This code performs the ECCSI/ Sakke dialogs as defined in RFCs 6507-6508.

    Output, with DEBUG output on and using RFC values, provides references out
    to the relevant RFCs for cross reference.

    Points to note:
        o It was/ is a personal project. It could do with a serious amount of 
          code review.
        o There is no interaction with a KMS or peers.
        o In es_demo_1 Alice and Bob both have the same ID (that is as per the 
          RFC).
        o In the es_demo_1 demo example a predefined message is signed, not 
          the encapsulated data. In ec-demo-2 the encapsulated data is signed 
          (as would more likely be the case).
        o It is C and OpenSSL (no other maths libraries), this makes it a tad
          slower, but hopefully more portable. 

    Other things to note with this implementation:
        o If you want to turn DEBUG output off, comment out the following line:
              #define ES_OUTPUT_DEBUG
          from lib/utils/log.h
        o If you want to change where data (community and user key data) you 
          will need to modify STORAGE_ROOT in inc/globals.h
        o If you want to use NON RFC values comment out the following line:
              #define ES_USE_RFC_VALUES
          from the demo/ test file es_demo_1.c and remake.

Making
------
    Prep (linux):
        The make script needs to be executable and as I am new to git hub,
        it does not seem immediately obvious how to (or even if you can) do 
        this. So, when you have cloned the repo, do:
        
           ./autogen.sh

           ./configure
        
     To make (linux):
     
        make
        
    Note! It is worth having a read of the make file as well. 

Running
-------
    To run:
        ./es_demo_1   -- contains RFC values.
        ./es_demo_2   -- different (non RFC) Alice and Bob values.

    Note! You will need to do the following first before running:
              export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:<path-to-where-you-installed>/lib
          refer to make script file for more details.

Doxygen
-------
    For doxygen documentation:

        Install:
            apt-get install -y graphviz
            apt-get install -y boost-graph
            apt-get install -y texlive
            apt-get install -y texlive-utils
            apt-get install -y doxygen

    Then:
        doxygen Doxyfile

    Next, web browser and open file:
        
        file://<path-to-this-dir>/doxygen_output/html/index.html

Contact Details
---------------
    yunhao.wang<AT>blockchain in lenovo
