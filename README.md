PHPDocumentor MarkDown export
=============================
Installation
------------
Install phpDocumentor:

    sudo pear channel-discover pear.phpdoc.org
    sudo pear install phpdoc/phpDocumentor

Install Composer:

    curl -sS https://getcomposer.org/installer | sudo php -- --filename=composer --install-dir=/usr/bin

Clone this repo:

    git clone git@github.com:angeldeejay/phpdoc-md.git phpdoc-md
    
Setup:

    cd phpdoc-md
    composer install --dev
    sudo ln -fsv `pwd | awk '{printf $0"/bin/execute"}'` /usr/bin/phpdoc_md
    sudo ln -fsv `pwd | awk '{printf $0"/bin/phpdocmd"}'` /usr/bin/


Usage
-----

    phpdoc_md -t TARGET [-d PATH|-f FILEPATH]


Options
-------

    -t TARGET
        Output dir.
    -d PATH
        Library path. Usefull when you wanna export all files in a folder
        and subfolders
    -f FILENAME
        Export single file
