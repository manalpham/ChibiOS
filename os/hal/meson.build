subdir('boards')
subdir('osal')
subdir('ports')

hal_includes = include_directories(['include',])
hal_sources = [ 'src/hal.c',
            	'src/hal_st.c',
            	'src/hal_buffers.c',
            	'src/hal_queues.c',
            	'src/hal_flash.c',
            	'src/hal_mmcsd.c',
            	'src/hal_adc.c',
            	'src/hal_can.c',
            	'src/hal_crypto.c',
            	'src/hal_dac.c',
            	'src/hal_efl.c',
            	'src/hal_gpt.c',
            	'src/hal_i2c.c',
            	'src/hal_i2s.c',
            	'src/hal_icu.c',
            	'src/hal_mac.c',
            	'src/hal_mmc_spi.c',
            	'src/hal_pal.c',
            	'src/hal_pwm.c',
            	'src/hal_rtc.c',
            	'src/hal_sdc.c',
            	'src/hal_serial.c',
            	'src/hal_serial_usb.c',
            	'src/hal_sio.c',
            	'src/hal_spi.c',
            	'src/hal_trng.c',
            	'src/hal_uart.c',
            	'src/hal_usb.c',
            	'src/hal_wdg.c',
            	'src/hal_wspi.c', ]

hal_dependencies = [ cfg,
		     hal_port, ]

hal = declare_dependency(dependencies : hal_dependencies,
			 include_directories : hal_includes,
			 sources : hal_sources)
