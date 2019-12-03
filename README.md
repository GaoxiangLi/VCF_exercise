#Simple VCF exercise:

Shawn Li 

  function:sort keyvalue in the VCF file
  Python version:3.68
  No other libiary needed.

How to use:
  1.Download and unzip

  2.input command line at root file path: 
                  
                  python vcf --sort 
                  --key KEY_NAME 
                  --filename FILENAME
                  --saved_path SAVED_PATH 
                  --order AES OR DES
                  --h  call for help 

  3.Sorted file will be created at: ./data/SortByKEY_NAME.vcf 

    filename: default as small_demo.vcf
    order:default as AES
    saved_path default as ./data/

     Simple example: python vcf --sort --key BaseQRankSum
     Simple example: python vcf --sort --key BaseRankSum --svaed_path ./result/ --order AES

Notice: some Key cannot be used since some data mistakes
example: At 441 line, AC values 1,1. So this cannot be convert to float and used to sort.

      TimSort algorithm is used. It's a stable sort which I think should be important for research. 


