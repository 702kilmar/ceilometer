# ceilometer
# 
# Test
cd /opt/stack/ceilometer

sudo tox -e py27 -- ceilometer.tests.unit.publisher.test_file

# reinstall
cd /opt/stack/ceilometer

sudo python setup.py install 

sudo systemctl restart devstack@ceilometer-anotification.service

sudo systemctl restart devstack@*

sudo  journalctl -f -u devstack@ceilometer-anotification.service
