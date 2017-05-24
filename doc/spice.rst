.. _spicepage:

SPICE 
=================


SPICE_ is an information system, built by the Navigation and Ancillary Information Facility (NAIF),  under the directions of NASA's Planetary Science Division. All the information contained in this chapeter is a summary from the `NAIF web site <https://naif.jpl.nasa.gov/naif/index.html>`_

.. _SPICE: https://naif.jpl.nasa.gov/naif/aboutspice.html 


Kernels
--------------------------

Kernels are ancillary data for SPICE. They are divided in cathegories,
accoring to their functionalities. For the goal of this work, we only a subset of available kernels:

- Spacecraft and Planet Ephemeris (SPK)
- Planetary Constants, for natural bodies,with orientation,size and shape (PCK);
- leapseconds (LSK)
- reference frame specifications(FK)

Through the `NAIF web site <https://naif.jpl.nasa.gov/naif/index.html>`_ three kind of 
kernels are available:

- PDS Archived SPICE Data Sets;
- Operational Flight Projects Kernels and Other Non-archived Project Kernels;
- Generic Kernels;



Cspice
----------------------------

Cspice is a ANSI C version of SPICE. It is designed to mimic the FORTRAN routines of SPICE.
The API allows cover a wide set of functions. Among these there are fuctions for  kernels handling, translation between coordinate systems, rotation funtctions.
Full description is in `CSPICE web page <https://naif.jpl.nasa.gov/pub/naif/toolkit_docs/C/index.html>`_




Utilities
----------------------------

Pinpoint is a NAIF utility to generate ephemeris for any object with constant
position or velocity with respect a SPICE reference frame. This can be done to generate 
proper ephemeris for topocentric locations.
The ephemerides of DSN network  are available from 



.. code:: bash


    ./pinpoint -spk srt.bsp \
               -fk srt.bsk \
               -pck  pck00010.tpc \
               -pck earth_latest_high_prec.bpc \
               -def srt.def
               


