# The central verdict server for VyPR

When a program is monitored with VyPR, the server with which VyPR interacts is this one.  This provides insertion and querying APIs.

## Setup

Once you've cloned this repository, you need to setup the verdict database.  For now, we use sqlite.  Run:

`sqlite3 verdicts.db < verdict-schema.sql`

to create the database file to which the server will write when it receives instrumentation and monitoring information from VyPR.

Finally, the server needs the Python 3 version of VyPR (http://github.com/pyvypr/VyPR-py3/) to be placed in the root directory of the server (eg, `VyPRServer/VyPR`).  Note that the version of VyPR needed by the server doesn't require you to follow any of the usual setup steps since VyPR is only needed on the server for certain classes it contains.

**VyPR must be found in the directory `VyPR/` in the root directory of the project.**


## Licence

(C) Copyright 2018 CERN and University of Manchester.
This software is distributed under the terms of the GNU General Public Licence version 3 (GPL Version 3), copied verbatim in the file "COPYING".
In applying this licence, CERN does not waive the privileges and immunities granted to it by virtue of its status as an Intergovernmental Organization or submit itself to any jurisdiction.

Author: Joshua Dawes - CERN, University of Manchester
