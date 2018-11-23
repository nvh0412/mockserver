# Mountebank Docker Image

Provides [mountebank](http://www.mbtest.org/).

Installs the latest version of mountebank and exposes port 2525 ready for
configuration and testing.

Visiting [localhost:2525](http://localhost:2525).

If you wish to load your imposters automatically, mount your imposters as a
volume and bind the necessary ports:

    docker run \
        -v ./imposters:/imposters \
        [-p IMPOSTER_1_PORT:IMPOSTER_1_PORT ...] \
        -p 2525:2525 \
        -d thinkei/mountebank \
        --configfile /imposters/imposters.ejs --allowInjection
