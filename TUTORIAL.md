# Getting startet
This is a complete tutorial which will guide you into getting your own history animation. It's build on a fresh Debian 6.0.3 installation.

## installing the packages
First off, you'll need a set of packages:

    sudo aptitude install postgresql postgresql-contrib postgis zlib1g-dev libexpat1 libexpat1-dev libxml2 libxml2-dev \
        libgeos-dev libprotobuf6 libprotobuf-dev protobuf-compiler libsparsehash-dev libboost-dev libgdal1-dev subversion \
        git build-essential

## getting and building the tools
Next, you'll want to download and build the history-splitter and the history-renderer.
First, get and build the osm-pbf lib:

    git clone https://github.com/scrosby/OSM-binary.git
    cd OSM-binary/src
    make
    sudo make install
    cd ../..

Next, get and build the splitter:

    git clone https://github.com/MaZderMind/osm-history-splitter.git
    cd osm-history-splitter
    git submodule init
    git submodule update
    make
    sudo make install
    cd ..

Next one will be the importer and renderer:

    git clone https://github.com/MaZderMind/osm-history-renderer.git
    cd osm-history-renderer
    git submodule init
    git submodule update
    cd importer
    make
    sudo make install
    cd ../..

## cutting your area
 Most people will want to create their own extract before rendering, so we'll cover this step here, too. Go to 

## importing

## getting the style

## rendering