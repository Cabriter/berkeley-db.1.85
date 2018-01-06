# berkeley-db.1.85
berkeley db.1.85
#	@(#)README	8.27 (Berkeley) 9/1/94

This is version 1.85 of the Berkeley DB code.

For information on compiling and installing this software, see the file
PORT/README.

Newer versions of this software will periodically be made available by
anonymous ftp from ftp.cs.berkeley.edu.  An archive in compressed format
is in ucb/4bsd/db.tar.Z, or in gzip format in ucb/4bsd/db.tar.gz.  If
you'd like to receive announcements of future releases of this software,
send email to the contact address below.

Email questions may be addressed to Keith Bostic at bostic@cs.berkeley.edu.

============================================
Distribution contents:

Makefile.inc	Ignore this, it's the 4.4BSD subsystem Makefile.
PORT		The per OS/architecture directories to use to build
		libdb.a, if you're not running 4.4BSD.  See the file
		PORT/README for more information.
README		This file.
btree		The B+tree routines.
changelog	List of changes, per version.
db		The dbopen(3) interface routine.
docs		Various USENIX papers, and the formatted manual pages.
hash		The extended linear hashing routines.
man		The unformatted manual pages.
mpool		The memory pool routines.
recno		The fixed/variable length record routines.
test		Test package.

============================================
Debugging:

If you're running a memory checker (e.g. Purify) on DB, make sure that
you recompile it with "-DPURIFY" in the CFLAGS, first.  By default,
allocated pages are not initialized by the DB code, and they will show
up as reads of uninitialized memory in the buffer write routines.
