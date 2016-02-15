nbravos_version from https://github.com/nbravo/evaluate with slight modifications

For original README, see ORIGINAL_README

0. Make sure you run 'source path.sh' to set environment variables. Depending on how files have changed, this may be outdated so you may 	have to find where the scripts are.



1. Run the decoder using ./decode_and evaluate.sh 0 conf/gale.conf 
	or ./decode_and evaluate.sh 0 conf/nutrition.conf



2. Follow below if you would like to change the wav files to decode

#--- Using conf/gale.conf ---

2.1a. Specify files in /data/sls/scratch/nbravo/kaldi/egs/gale_arabic.complete/s5/data/test/split30/nbravo/spk2utt
	THe numbers at the end (_1006200_1013930) represent time stamps

2.2a. Specify files in /data/sls/scratch/nbravo/kaldi/egs/gale_arabic.complete/s5/data/test/split30/nbravo/wav.scp
	This uses file paths in the directory /data/sls/scratch/amali/data/GALE/LDC2013S02/gale_p2_arb_bc_speech_p1_d1/data/. So if you want to add more files, use them from this path

2.3a. Specify /data/sls/scratch/nbravo/kaldi/egs/gale_arabic.complete/s5/data/test/split30/nbravo/segments. I am unsure of what the numbers are supposed to mean, particularly the _1006200_1013930 at the end of the filenames.

Note: Yes, this is nbravo's directory which may change at any point in time. And yes you must specify individual files unless you write a script to do batches. 

#--- Using conf/nutrition.conf ---

Go to conf/nutrition.conf and change

2.1b. SPK2UTT path: 	/data/sls/scratch/pricem/kaldi/nutrition/data/test_amt1/split10/ *vary this number from 1-10* /spk2utt

2.2b. WAV path:     	/data/sls/scratch/pricem/kaldi/nutrition/data/test_amt1/split10/ *put the same number* /wav.scp

Note: This does batches of wav files. 

#----------------------------------



3.  Look at the step 1.


Notes: 
	Haven't figured out how to make ./recognize work. But it is just a running lots of ./decode_and_evaluate.
	All credit to nbravo. 