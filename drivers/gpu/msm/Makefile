ccflags-y := -Iinclude/drm

msm_kgsl_core-y = \
	kgsl.o \
	kgsl_sharedmem.o \
	kgsl_pwrctrl.o

msm_kgsl_core-$(CONFIG_DEBUG_FS) += kgsl_debugfs.o
msm_kgsl_core-$(CONFIG_MSM_KGSL_MMU) += kgsl_mmu.o
msm_kgsl_core-$(CONFIG_MSM_KGSL_CFF_DUMP) += kgsl_cffdump.o
msm_kgsl_core-$(CONFIG_MSM_KGSL_DRM) += kgsl_drm.o

msm_adreno-y += \
	adreno_ringbuffer.o \
	adreno_drawctxt.o \
	adreno_postmortem.o \
	adreno.o

msm_adreno-$(CONFIG_DEBUG_FS) += adreno_debugfs.o

msm_kgsl_core-objs = $(msm_kgsl_core-y)
msm_adreno-objs = $(msm_adreno-y)

obj-y += \
	msm_kgsl_core.o \
	msm_adreno.o
