Distribution.Broensfin
======================


    git clone https://github.com/mneuhaus/Distribution.Broensfin.git Broensfin
    cd Broensfin
    composer install
    beard patch

Migrate your database:

    ./flow doctrine:migrate

Prune an existing site (we are working on a seamless update):

    ./flow site:prune --confirmation TRUE

To get started the Neos demo site should be imported:

    ./flow site:import --package-key TYPO3.NeosDemoTypo3Org

As a default every node will be assigned to the "mul_ZZ" locale which is the default value in the context. To create
new variants of the nodes in another you can use a simple command for now:

    ./flow node:translate "/sites/neosdemotypo3org" TRUE "mul_ZZ" "de_DE"
