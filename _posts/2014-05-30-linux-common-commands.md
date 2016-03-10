---
layout: post
title:  "Linux Common Commands"
date:   2014-05-30
categories: tech
---

## cd
* cd - #change current path to previous path.

## ls
* ls -1  #only list the filename per line.

## cut
* cut -d '\t' -f 1,2

## grep
* grep -o ',' | wc -l  #count the occurrences of one substr in string.

## sort
* sort -t$'\t' -k5 -n

## awk & sed
* awk 'BEGIN {srand()} !/^$/ { if (rand() <= .01) print $0}'
* sed -n '2,2p'
* sed  '/^$/d'

## ssh

	$ ssh-keygen -t rsa
	$ ssh b@B mkdir -p .ssh
	$ cat .ssh/id_rsa.pub | ssh b@B 'cat >> .ssh/authorized_keys'

## readline
* ctrl + w # delete the word before the cursort.

## rsync
* rsync --exclude #exclude some file

## tar
* tar -xvf #untar
* tar -cvf /tmp/etc.tar /etc #tar, not compressed
* tar -zcvf /tmp/etc.tar.gz /etc #tar, compressed with gzip
* tar -jcvf /tmp/etc.tar.bz2 /etc #tar, compressed with bzip2

## Shell
{% highlight bash %}
declare -a array=(a b)
for item in ${array[@]}
do

done
{% endhighlight %}
