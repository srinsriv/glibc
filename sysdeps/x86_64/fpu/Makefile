ifeq ($(subdir),mathvec)
libmvec-support += svml_d_cos2_core svml_d_cos4_core_avx \
		   svml_d_cos4_core svml_d_cos8_core \
		   svml_d_sin2_core svml_d_sin4_core_avx \
		   svml_d_sin4_core svml_d_sin8_core svml_d_trig_data \
		   svml_s_cosf4_core svml_s_cosf8_core_avx \
		   svml_s_cosf8_core svml_s_cosf16_core svml_s_trig_data \
		   svml_s_sinf4_core svml_s_sinf8_core_avx \
		   svml_s_sinf8_core svml_s_sinf16_core \
		   svml_d_sincos2_core svml_d_sincos4_core_avx \
		   svml_d_sincos4_core svml_d_sincos8_core \
		   svml_d_log2_core svml_d_log4_core_avx svml_d_log4_core \
		   svml_d_log8_core svml_d_log_data svml_s_logf4_core \
		   svml_s_logf8_core_avx svml_s_logf8_core svml_s_logf16_core \
		   svml_s_logf_data svml_d_exp2_core svml_d_exp4_core_avx \
		   svml_d_exp4_core svml_d_exp8_core svml_d_exp_data \
		   svml_s_expf4_core svml_s_expf8_core_avx svml_s_expf8_core \
		   svml_s_expf16_core svml_s_expf_data svml_d_pow2_core \
		   svml_d_pow4_core_avx svml_d_pow4_core svml_d_pow8_core \
		   svml_d_pow_data svml_s_powf4_core svml_s_powf8_core_avx \
		   svml_s_powf8_core svml_s_powf16_core svml_s_powf_data \
		   svml_s_sincosf4_core svml_s_sincosf8_core_avx \
		   svml_s_sincosf8_core svml_s_sincosf16_core svml_finite_alias

libmvec-static-only-routines = svml_finite_alias
endif

# Variables for libmvec tests.
ifeq ($(subdir),math)
ifeq ($(build-mathvec),yes)
libmvec-tests += double-vlen2 double-vlen4 double-vlen4-avx2 \
		 float-vlen4 float-vlen8 float-vlen8-avx2
tests += test-double-libmvec-alias test-double-libmvec-alias-avx \
	 test-double-libmvec-alias-avx2 test-double-libmvec-alias-main \
	 test-double-libmvec-alias-avx-main test-double-libmvec-alias-avx2-main \
	 test-float-libmvec-alias test-float-libmvec-alias-avx \
	 test-float-libmvec-alias-avx2 test-float-libmvec-alias-main \
	 test-float-libmvec-alias-avx-main test-float-libmvec-alias-avx2-main \
	 test-double-libmvec-sincos test-double-libmvec-sincos-avx \
	 test-double-libmvec-sincos-avx2 test-float-libmvec-sincosf \
	 test-float-libmvec-sincosf-avx test-float-libmvec-sincosf-avx2
modules-names += test-double-libmvec-alias-mod \
		 test-double-libmvec-alias-avx-mod \
		 test-double-libmvec-alias-avx2-mod \
		 test-float-libmvec-alias-mod \
		 test-float-libmvec-alias-avx-mod \
		 test-float-libmvec-alias-avx2-mod
test-double-libmvec-alias-mod.so-no-z-defs = yes
test-double-libmvec-alias-avx-mod.so-no-z-defs = yes
test-double-libmvec-alias-avx2-mod.so-no-z-defs = yes
test-float-libmvec-alias-mod.so-no-z-defs = yes
test-float-libmvec-alias-avx-mod.so-no-z-defs = yes
test-float-libmvec-alias-avx2-mod.so-no-z-defs = yes

$(objpfx)test-double-libmvec-alias: \
  $(objpfx)test-double-libmvec-alias-mod.so
$(objpfx)test-double-libmvec-alias-mod.so: \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-double-libmvec-alias-avx: \
  $(objpfx)test-double-libmvec-alias-avx-mod.so
$(objpfx)test-double-libmvec-alias-avx-mod.so: \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-double-libmvec-alias-avx2: \
  $(objpfx)test-double-libmvec-alias-avx2-mod.so
$(objpfx)test-double-libmvec-alias-avx2-mod.so: \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-double-libmvec-alias-main: \
  $(objpfx)test-double-libmvec-alias-mod.os \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-double-libmvec-alias-avx-main: \
  $(objpfx)test-double-libmvec-alias-avx-mod.os \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-double-libmvec-alias-avx2-main: \
  $(objpfx)test-double-libmvec-alias-avx2-mod.os \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-float-libmvec-alias: \
  $(objpfx)test-float-libmvec-alias-mod.so
$(objpfx)test-float-libmvec-alias-mod.so: \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-float-libmvec-alias-avx: \
  $(objpfx)test-float-libmvec-alias-avx-mod.so
$(objpfx)test-float-libmvec-alias-avx-mod.so: \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-float-libmvec-alias-avx2: \
  $(objpfx)test-float-libmvec-alias-avx2-mod.so
$(objpfx)test-float-libmvec-alias-avx2-mod.so: \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-float-libmvec-alias-main: \
  $(objpfx)test-float-libmvec-alias-mod.os \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-float-libmvec-alias-avx-main: \
  $(objpfx)test-float-libmvec-alias-avx-mod.os \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-float-libmvec-alias-avx2-main: \
  $(objpfx)test-float-libmvec-alias-avx2-mod.os \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-double-libmvec-sincos: \
  $(objpfx)test-double-libmvec-sincos.o $(libmvec)

$(objpfx)test-double-libmvec-sincos-avx: \
  $(objpfx)test-double-libmvec-sincos-avx.o $(libmvec)

$(objpfx)test-double-libmvec-sincos-avx2: \
  $(objpfx)test-double-libmvec-sincos-avx2.o $(libmvec)

$(objpfx)test-float-libmvec-sincosf: \
  $(objpfx)test-float-libmvec-sincosf.o $(libmvec)

$(objpfx)test-float-libmvec-sincosf-avx: \
  $(objpfx)test-float-libmvec-sincosf-avx.o $(libmvec)

$(objpfx)test-float-libmvec-sincosf-avx2: \
  $(objpfx)test-float-libmvec-sincosf-avx2.o $(libmvec)

ifeq (yes,$(config-cflags-avx512))
libmvec-tests += double-vlen8 float-vlen16
tests += test-double-libmvec-alias-avx512 \
	 test-float-libmvec-alias-avx512 \
	 test-double-libmvec-alias-avx512-main \
	 test-float-libmvec-alias-avx512-main \
	 test-double-libmvec-sincos-avx512 \
	 test-float-libmvec-sincosf-avx512
modules-names += test-double-libmvec-alias-avx512-mod \
		 test-float-libmvec-alias-avx512-mod
test-double-libmvec-alias-avx512-mod.so-no-z-defs = yes
test-float-libmvec-alias-avx512-mod.so-no-z-defs = yes

$(objpfx)test-double-libmvec-alias-avx512: \
  $(objpfx)test-double-libmvec-alias-avx512-mod.so
$(objpfx)test-double-libmvec-alias-avx512-mod.so: \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-double-libmvec-alias-avx512-main: \
  $(objpfx)test-double-libmvec-alias-avx512-mod.os \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-float-libmvec-alias-avx512: \
  $(objpfx)test-float-libmvec-alias-avx512-mod.so
$(objpfx)test-float-libmvec-alias-avx512-mod.so: \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-float-libmvec-alias-avx512-main: \
  $(objpfx)test-float-libmvec-alias-avx512-mod.os \
  $(objpfx)../mathvec/libmvec_nonshared.a $(libmvec)

$(objpfx)test-double-libmvec-sincos-avx512: \
  $(objpfx)test-double-libmvec-sincos-avx512.o $(libmvec)

$(objpfx)test-float-libmvec-sincosf-avx512: \
  $(objpfx)test-float-libmvec-sincosf-avx512.o $(libmvec)
endif

double-vlen4-arch-ext-cflags = -mavx
double-vlen4-arch-ext2-cflags = -mavx2
double-vlen8-arch-ext-cflags = -mavx512f

float-vlen8-arch-ext-cflags = -mavx
float-vlen8-arch-ext2-cflags = -mavx2
float-vlen16-arch-ext-cflags = -mavx512f

libmvec-sincos-cflags = $(libm-test-fast-math-cflags) -fno-inline -fopenmp -Wno-unknown-pragmas
libmvec-alias-cflags = $(libmvec-sincos-cflags) -ffloat-store -ffinite-math-only

CFLAGS-test-double-libmvec-alias-mod.c = $(libmvec-alias-cflags)
CFLAGS-test-double-libmvec-alias-avx-mod.c = $(double-vlen4-arch-ext-cflags) $(libmvec-alias-cflags) -DREQUIRE_AVX
CFLAGS-test-double-libmvec-alias-avx2-mod.c = $(double-vlen4-arch-ext2-cflags) $(libmvec-alias-cflags) -DREQUIRE_AVX2
CFLAGS-test-double-libmvec-alias-avx512-mod.c = $(double-vlen8-arch-ext-cflags) $(libmvec-alias-cflags) -DREQUIRE_AVX512F

CFLAGS-test-float-libmvec-alias-mod.c = $(libmvec-alias-cflags)
CFLAGS-test-float-libmvec-alias-avx-mod.c = $(double-vlen4-arch-ext-cflags) $(libmvec-alias-cflags) -DREQUIRE_AVX
CFLAGS-test-float-libmvec-alias-avx2-mod.c = $(double-vlen4-arch-ext2-cflags) $(libmvec-alias-cflags) -DREQUIRE_AVX2
CFLAGS-test-float-libmvec-alias-avx512-mod.c = $(double-vlen8-arch-ext-cflags) $(libmvec-alias-cflags) -DREQUIRE_AVX512F

CFLAGS-test-double-vlen4-avx2.c = $(libm-test-vec-cflags)
CFLAGS-test-double-vlen4-avx2-wrappers.c = $(double-vlen4-arch-ext2-cflags)

CFLAGS-test-float-vlen8-avx2.c = $(libm-test-vec-cflags)
CFLAGS-test-float-vlen8-avx2-wrappers.c = $(float-vlen8-arch-ext2-cflags)

CFLAGS-test-double-libmvec-sincos.c = $(libmvec-sincos-cflags)
CFLAGS-test-double-libmvec-sincos-avx.c = $(libmvec-sincos-cflags) $(double-vlen4-arch-ext-cflags) -DREQUIRE_AVX
CFLAGS-test-double-libmvec-sincos-avx2.c = $(libmvec-sincos-cflags) $(double-vlen4-arch-ext2-cflags) -DREQUIRE_AVX2
CFLAGS-test-double-libmvec-sincos-avx512.c = $(libmvec-sincos-cflags) $(double-vlen8-arch-ext-cflags) -DREQUIRE_AVX512F

CFLAGS-test-float-libmvec-sincosf.c = $(libmvec-sincos-cflags)
CFLAGS-test-float-libmvec-sincosf-avx.c = $(libmvec-sincos-cflags) $(float-vlen8-arch-ext-cflags) -DREQUIRE_AVX
CFLAGS-test-float-libmvec-sincosf-avx2.c = $(libmvec-sincos-cflags) $(float-vlen8-arch-ext2-cflags) -DREQUIRE_AVX2
CFLAGS-test-float-libmvec-sincosf-avx512.c = $(libmvec-sincos-cflags) $(float-vlen16-arch-ext-cflags) -DREQUIRE_AVX512F
endif
endif
