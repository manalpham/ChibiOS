project('demo', 'c')

inc = []
src = []

subdir('os/common')
subdir('os/license')
subdir('demos/STM32/RT-STM32L452RE-NUCLEO64/cfg')
subdir('os/oslib')
subdir('os/rt')
subdir('os/hal')
subdir('demos/STM32/RT-STM32L452RE-NUCLEO64')


inc += license_inc
inc += oslib_inc
inc += rt_inc

src += oslib_src
src += rt_src

exe = executable('demo',
	    	 include_directories : inc,
	    	 sources : src,
	    	 dependencies : demo,
	    	 name_suffix : 'elf',
	    	 install_dir : meson.source_root() + '/build')

bin = custom_target('bin',
		    input : exe,
		    output : '@0@.bin'.format('demo'),
		    depends: exe,
    		    command: [ 'arm-none-eabi-objcopy', '-O', 'binary', '@INPUT@', '@OUTPUT@' ],
    		    console : true,
    		    build_by_default: true)

hex = custom_target('hex',
		    input : exe,
		    output : '@0@.hex'.format('demo'),
		    depends: exe,
    		    command: [ 'arm-none-eabi-objcopy', '-O', 'ihex', '@INPUT@', '@OUTPUT@' ],
    		    console : true,
    		    build_by_default: true)

custom_target('size',
    	      input : exe,
	      output : '@0@.size'.format('demo'),
	      depends: exe,
    	      command: [ 'arm-none-eabi-size', '@INPUT@' ],
    	      console : true,
    	      build_by_default: true)

custom_target('flash',
	      input : bin,
	      output : '@0@.flash'.format('demo'),
	      depends : bin,
	      command : ['st-flash', 'write', '@INPUT@', '0x8000000'],
	      console : true,
              build_by_default : true)
