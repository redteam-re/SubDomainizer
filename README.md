## SubDomainizer
SubDomainizer is a tool designed to find hidden subdomains present is either inline javascript or external javascripts present in the given URL.
This tool also finds S3 buckets and cloudfront URL's from those JS files which could be interesting like S3 bucket is open to read/write, or subdomain takeover and similar case for cloudfront.

## Screenshot:

![SubDomainizer](https://i.imgur.com/x3XSamk.png)

## Installation Steps

1. Clone SubDomainzer from git:
```
git clone https://github.com/nsonaniya2010/SubDomainizer.git
```
2. Install the requirements:

```
sudo apt-get update
sudo apt-get install python3-termcolor python3-bs4 python3-requests python3-htmlmin python3-tldextract
```
3. Enjoy the Tool.


## Usage

Short Form    | Long Form     | Description
------------- | ------------- |-------------
-u            | --url         | URL in which you want to find (sub)domains.
-l            | --listfile    | File which contain list of URL's needs to be scanned.
-o            | --output      | Output file name in which you need to save the results.
-c            | --cookie      | Cookies which needs to be sent with request.
-h            | --help        | show the help message and exit.

### Examples
* To list help about the tool:
```
python3 SubDomainizer.py -h
```
* To find subdomains, s3 buckets, and cloudfront URL's for given single URL:
```
python3 SubDomainizer.py -u http://www.example.com
```
* To find subdomains from given list of URL (file given):
```
python3 SubDomainizer.py -l list.txt
```

* To save the results in (output.txt) file:
```
python3 SubDomainizer.py -u https://www.example.com -o output.txt
```
* To give cookies:
```
python3 SubDomainizer.py -u https://www.example.com -c "test=1; test=2"
```
