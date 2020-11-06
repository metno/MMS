# Client COmmands

[ [Back to README](README.md) ]

## Get some information

`mms config show`

## Send a message

### Implicitly defined
* production hub
* timestamp
* Product (name, can be derived from filename by removing timestamp)

### Needs to be defined (choices)
* path
* parent dataset

`mms post --file meps_det_2_5km_20200821T06Z.ncml`