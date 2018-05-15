# ceilometer
# 
# Test
cd /opt/stack/ceilometer

sudo tox -e py27 -- ceilometer.tests.unit.publisher.test_file

# reinstall
cd /opt/stack/ceilometer

sudo python setup.py install 

