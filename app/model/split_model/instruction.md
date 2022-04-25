To bypass PythonAnywhere file size limit 

Split a file with command
`split -b 50m FILENAME PREFIX`

join them with 
`cat PREFIX?? > FILENAME`

`??` matches file with PREFIX 

you want the filename of the joined file to be `pytorch_model.bin`
