AM_CPPFLAGS = -Wconversion
LIBSVM_SHARED_LIB_VERSION = @LIBSVM_SHARED_LIB_VERSION@

bin_PROGRAMS = svm-predict svm-train svm-scale

svm_predict_SOURCES = svm-predict.c
svm_train_SOURCES = svm-train.c
svm_scale_SOURCES = svm-scale.c

svm_predict_LDADD = svm.$(OBJEXT) -lstdc++
svm_train_LDADD = svm.$(OBJEXT) -lstdc++
svm_scale_LDADD = svm.$(OBJEXT) -lstdc++

lib_LTLIBRARIES = libsvm.la
libsvm_la_SOURCES = svm.cpp
libsvm_la_LDFLAGS = -version-info $(LIBSVM_SHARED_LIB_VERSION)

libsvm_include_HEADERS = svm.h
libsvm_includedir=$(includedir)
