dnl macro: AC_INIT (package, version, [bug-report], [tarname], [url])
dnl Process any command line arguments and perform various initializations and
dnl verifications.
AC_INIT([char80], [0.1], [mdddmmmm@yandex.ru])

dnl macro: AM_INIT_AUTOMAKE ([options])
dnl Runs many macros required for proper operatioin of the generated Makefiles
dnl Today, AM_INIT_AUTOMAKE is called with a single argument: a space-separated
dnl list of Automake options that should be applied to every Makefile.am in the
dnl tree. The effect is as if each option were listed in AUTOMAKE_OPTIONS
dnl note: this has nothing to deal with gcc flags.
dnl possible strictness options: cygnus, foreign, gnu, gnits (from less to more
dnl							      strict)
AM_INIT_AUTOMAKE([-Wall -Werror gnits])

: ${CFLAGS=""}

dnl macro: AC_PROG_CC ([compiler-search-list])
dnl Determine a C compiler to use. If cc is not already set in the environment,
dnl check for gcc and cc, then for other C compilers. Set output variable cc to
dnl the name of the compiler found
AC_PROG_CC

dnl macro: AC_CONFIG_HEADERS (header ..., [cmds], [init-cmds])
dnl This macro is 1 of the instantiating macros. Make AC_OUTPUT create the
dnl file(s) in the blank-or-newline-separated list header containing c
dnl preprocessor #define statements, and replace '@DEFS@' in generated files
dnl with -DHAVE_CONFIG_H instead of the value of DEFS. The usual name for
dnl header is config.h
AC_CONFIG_HEADERS([config.h])

dnl macro: AC_CONFIG_FILES (file ..., [cmds], [init-cmds])
dnl Make AC_OUTPUT create each file by copying an input file
dnl (by default file.in), substituting the output variable values. This macro
dnl is one of the instantiating macros. This macro creates the directory that
dnl the file is in if it does not exist. Usually, makefiles are created this
dnl way, but other files, such as .gdbinit, can be specified as well.
dnl Typical calls to AC_CONFIG_FILES look like this:
dnl AC_CONFIG_FILES([Makefile src/Makefile man/Makefile X/Imakefile])
dnl AC_CONFIG_FILES([[autoconf], [chmod +x autoconf]])
AC_CONFIG_FILES([
 Makefile
 src/Makefile
])

dnl macro: AC_OUTPUT
dnl Generate config.status and launch it. Call this macro once, at the end of
dnl configure.ac
dnl Config.status performs all the configuration actions: all the output files,
dnl header files, commands, links, subdirectories to configure are honored
AC_OUTPUT
