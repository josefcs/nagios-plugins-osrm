nagios-plugins-osrm
===================

Nagios plugins for osrm.
Taken from https://github.com/rodo/nagios-plugins-osrm and adapted.

Requirements
============

Usage
=====

* check_osrm_hello!PORT

* check_osrm_locate!PORT!LOCATION

* check_osrm_nearest!PORT!LOCATION

* check_osrm_viaroute!PORT!LOCATION_1!LOCATION_2

* check_osrm_viaroute_result!PORT!LOCATION_1!LOCATION_2

Sample

    define service {
        host_name                       osrm.quiedeville.org
        service_description             trucks
        check_command                   check_osrm_viaroute_result!5002!50.294,2.782!50.281,2.792
    }

Variables
=========

* **PORT** : the tcp port on which osrm listen

* **LOCATION** : coordinate as lat,lon as OSRM 



