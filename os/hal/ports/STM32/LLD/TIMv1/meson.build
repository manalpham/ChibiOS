hal_stm32_timv1_inc = include_directories( [ '.', ] )
hal_stm32_timv1_src = [ 'hal_gpt_lld.c',
	      		'hal_icu_lld.c',
	      		'hal_pwm_lld.c',
	      		'hal_st_lld.c', ]

hal_stm32_timv1 = declare_dependency(include_directories : hal_stm32_timv1_inc,
			             sources : hal_stm32_timv1_src)
