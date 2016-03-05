# Disable caching
define([AC_CACHE_LOAD], )
define([AC_CACHE_SAVE], )

# Init
AC_PREREQ(2.59)
AC_INIT([libantlr], 2.7.4, bugs@xmlpl.org)
AC_CONFIG_SRCDIR([config.h.in])
AC_CONFIG_AUX_DIR(./config)

AM_INIT_AUTOMAKE([nostdinc])
AM_CONFIG_HEADER(config.h)


# Tools
AC_PROG_LN_S
AC_LANG_CPLUSPLUS
AC_PROG_CXX
AC_PROG_CXXCPP
AC_PROG_INSTALL
AM_PROG_LIBTOOL


# Headers
AC_HEADER_STDC
AC_CHECK_HEADERS([stdlib.h string.h unistd.h])


# Typedefs, structures, and compiler characteristics
AC_HEADER_STDBOOL
AC_C_CONST
AC_C_INLINE


# Standard library functions
AC_FUNC_ERROR_AT_LINE
AC_FUNC_MALLOC
AC_FUNC_REALLOC
AC_CHECK_FUNCS([strchr strdup])


# Test install -C option
touch install.test
if $INSTALL -C install.test install.test2 >/dev/null 2>/dev/null; then
  INSTALL="${INSTALL} -C"
fi
rm -f install.test install.test2

# Create Makefiles
AC_OUTPUT([Makefile
	  src/Makefile
	  src/antlr/Makefile
	  scripts/Makefile
	  scripts/antlr-config
	  ], [chmod +x scripts/antlr-config]
         )

echo
echo
echo "   Everything seems to be ok."
echo "Now run 'make' and 'make install'."
echo
echo
