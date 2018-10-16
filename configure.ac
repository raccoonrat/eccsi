#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([eccsi], [0.1], [wangyh43@lenovo.com])
AC_CONFIG_SRCDIR([src/es_demo_2.c])
AC_CONFIG_HEADERS([config.h])

AM_INIT_AUTOMAKE
# Checks for programs.
AC_CONFIG_MACRO_DIRS([m4])
AC_PROG_AWK
AC_PROG_CC
LT_INIT
AC_PROG_LIBTOOL

# Checks for libraries.
# FIXME: Replace `main' with a function in `-lcore12':
AC_CHECK_LIB([crypto], [main])
AC_CHECK_LIB([core12], [main])
# FIXME: Replace `main' with a function in `-ldl':
AC_CHECK_LIB([dl], [main])
# FIXME: Replace `main' with a function in `-levent_core':
AC_CHECK_LIB([event_core], [main])
# FIXME: Replace `main' with a function in `-levent_extra':
AC_CHECK_LIB([event_extra], [main])
# FIXME: Replace `main' with a function in `-levent_pthreads':
AC_CHECK_LIB([event_pthreads], [main])
# FIXME: Replace `main' with a function in `-lipgo':
AC_CHECK_LIB([ipgo], [main])
# FIXME: Replace `main' with a function in `-lirc':
AC_CHECK_LIB([irc], [main])
# FIXME: Replace `main' with a function in `-lm':
AC_CHECK_LIB([m], [main])
# FIXME: Replace `main' with a function in `-lnls12':
AC_CHECK_LIB([nls12], [main])
# FIXME: Replace `main' with a function in `-lnnzst12':
AC_CHECK_LIB([nnzst12], [main])
# FIXME: Replace `main' with a function in `-lpthread':
AC_CHECK_LIB([pthread], [main])
# FIXME: Replace `main' with a function in `-lrt':
AC_CHECK_LIB([rt], [main])
# FIXME: Replace `main' with a function in `-lunls12':
AC_CHECK_LIB([ssl], [main])
AC_CHECK_LIB([unls12], [main])

# Checks for header files.
AC_CHECK_HEADERS([stdint.h stdlib.h string.h strings.h sys/time.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_C_INLINE
AC_TYPE_INT16_T
AC_TYPE_INT8_T
AC_TYPE_SIZE_T
AC_TYPE_UINT16_T
AC_TYPE_UINT8_T

# Checks for library functions.
AC_FUNC_REALLOC
AC_CHECK_FUNCS([gettimeofday memset strdup strncasecmp])

AC_CHECK_PROGS([DOXYGEN], [doxygen])
if test -z "$DOXYGEN"; then
   AC_MSG_WARN([Doxygen not found - continue without Doxygen support])
fi
AC_CHECK_PROGS([DOT], [dot])
if test -z "$DOT"; then
   AC_MSG_ERROR([Doxygen needs dot, please install dot first])
fi
AC_CHECK_PROGS([PDFLATEX], [pdflatex])
if test -z "$PDFLATEX"; then
   AC_MSG_ERROR([Doxygen needs pdflatex program, it is part of TeX http://www.tug.org/texlive/acquire-netinstall.html])
fi
AM_CONDITIONAL([HAVE_DOXYGEN], [test -n "$DOXYGEN"])
AM_COND_IF([HAVE_DOXYGEN], [AC_CONFIG_FILES([Doxyfile])])


AC_CONFIG_FILES([Makefile
                 lib/Makefile
                 src/Makefile])
AC_OUTPUT
