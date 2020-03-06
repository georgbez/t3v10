# t3v10 


https://ddev.readthedocs.io/en/latest/users/cli-usage/#typo3-quickstart

Init:

    mkdir t3v10
    cd t3v10
    echo "# t3v10" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin git@github.com:georgbez/t3v10.git
    git push -u origin master

Local install:

    ddev config --project-type=typo3 --docroot=public --create-docroot=true
    ddev start
    ddev composer create "typo3/cms-base-distribution:^10" --prefer-dist
    ddev start
    
DDEV Live:

    ddev-live create site typo3 georgbez/t3v10 --github-repo georgbez/t3v10 --docroot public --run-composer-install --typo3-version 10