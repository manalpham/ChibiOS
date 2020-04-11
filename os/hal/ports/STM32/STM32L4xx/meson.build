hal_stm32l4_includes = include_directories( [ '.', ] )

hal_stm32l4_sources = [ 'stm32_isr.c',
		    	'hal_lld.c',
		    	'hal_efl_lld.c', ]

hal_stm32l452 = [ hal_armcm_nvic,
	          hal_stm32_adcv3,
	      	  hal_stm32_canv1,
	      	  hal_stm32_dacv1,
	      	  hal_stm32_dmav1,
	      	  hal_stm32_extiv1,
	      	  hal_stm32_gpiov3,
	      	  hal_stm32_i2cv2,
	      	  hal_stm32_quadspiv1,
	      	  hal_stm32_rngv1,
	      	  hal_stm32_rtcv2,
	      	  hal_stm32_sdmmcv1,
	      	  hal_stm32_spiv2,
	      	  hal_stm32_timv1,
	      	  hal_stm32_usartv2,
	      	  hal_stm32_usbv1,
	      	  hal_stm32_xwdgv1, ]

hal_stm32l4 = declare_dependency(include_directories : hal_stm32l4_includes,
			     	 sources : hal_stm32l4_sources,
			     	 dependencies : hal_stm32l452)
