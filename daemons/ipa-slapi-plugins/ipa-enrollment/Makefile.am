NULL =

PLUGIN_COMMON_DIR = $(srcdir)/../common

AM_CPPFLAGS =							\
	-I$(srcdir)						\
	-I$(PLUGIN_COMMON_DIR)					\
	-DPREFIX=\""$(prefix)"\" 				\
	-DBINDIR=\""$(bindir)"\"				\
	-DLIBDIR=\""$(libdir)"\" 				\
	-DLIBEXECDIR=\""$(libexecdir)"\"			\
	-DDATADIR=\""$(datadir)"\"				\
	$(DIRSRV_CFLAGS)					\
	$(LDAP_CFLAGS)					\
	$(KRB5_CFLAGS)						\
	$(WARN_CFLAGS)						\
	$(NULL)

plugindir = $(libdir)/dirsrv/plugins
plugin_LTLIBRARIES = 			\
	libipa_enrollment_extop.la	\
	$(NULL)

libipa_enrollment_extop_la_SOURCES = 	\
	ipa_enrollment.c		\
	$(NULL)

libipa_enrollment_extop_la_LDFLAGS = -avoid-version

libipa_enrollment_extop_la_LIBADD = 	\
	$(LDAP_LIBS)			\
	$(NULL)

appdir = $(IPA_DATA_DIR)
app_DATA =			\
	enrollment-conf.ldif	\
	$(NULL)

EXTRA_DIST =			\
	$(app_DATA)		\
	$(NULL)
