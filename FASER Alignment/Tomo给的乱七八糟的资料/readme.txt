1, use globalalign branch
1.1 algorithm to extract derivations to a ntuple: https://gitlab.cern.ch/keli/calypso/-/blob/globalalign/Tracking/Acts/FaserActsKalmanFilter/src/CKF2GlobalAlignment.cxx
2, rebuild calypso:
2.1 cmake -DINSTALL_CONDB=ON -DCMAKE_INSTALL_PREFIX=../run ../calypso ; make -j install
3, make new database
3.1 prepare the bash script
3.1.1 ./maketemplate_data.sh
3.2 submit condor jobs
4 run millepede-ii : https://www.desy.de/~kleinwrt/MP2/doc/html/index.html
4.1 install millepede
4.2 convert ntuple to mille format: convert2mille_v2.C
4.3 runpede, ./pede mp2strfaser_data22_noIFT.txt
