AM_CPPFLAGS = $(SDL_CFLAGS) $(WZ_CPPFLAGS) $(QT4_CFLAGS)
AM_CFLAGS = $(WZ_CFLAGS)
AM_CXXFLAGS = $(WZ_CXXFLAGS) $(QT4_CFLAGS)

# Signals/slots
MOCHEADER = \
	bar.h \
	button.h \
	editbox.h \
	form.h \
	label.h \
	listwidget.h \
	slider.h \
	tip.h \
	widgbase.h \
	widget.h \
	widgint.h
MOCEDFILES = $(MOCHEADER:%.h=%_moc.cpp)
%_moc.cpp: %.h
	$(MOC4) -o $@ $<
CLEANFILES = \
	$(MOCEDFILES)

noinst_LIBRARIES = libwidget.a
noinst_HEADERS = \
	$(MOCHEADER)

#"nodist_libwidget_a_SOURCES = $(MOCEDFILES)" doesn't work here (not sure why).
nodist_libwidget_a_SOURCES = \
	bar_moc.cpp \
	button_moc.cpp \
	editbox_moc.cpp \
	form_moc.cpp \
	label_moc.cpp \
	listwidget_moc.cpp \
	slider_moc.cpp \
	tip_moc.cpp \
	widgbase_moc.cpp \
	widget_moc.cpp \
	widgint_moc.cpp

libwidget_a_SOURCES = \
	bar.cpp \
	button.cpp \
	editbox.cpp \
	form.cpp \
	label.cpp \
	listwidget.cpp \
	slider.cpp \
	tip.cpp \
	widget.cpp
