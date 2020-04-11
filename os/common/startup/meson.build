subdir('ARMCMx')

startup_inc = []
startup_src = []
startup_ld_arg = []


# portability - gcc
startup_inc += portability_gcc_inc

# ext - arm cmsis corem
startup_inc += ext_arm_cmsis_corem_inc
# ext - stm32l4
startup_inc += ext_st_stm32l4_inc

# armcmx - stm32l4
startup_inc += startup_armcmx_stm32l4_inc

# armcmx - gcc
startup_src += startup_armcmx_v7m_gcc_src

inc += startup_inc
src += startup_src


# linker script
startup_ld_arg += '-L' + startup_armcmx_gcc_ld_path
startup_ld_arg += '-T' + startup_armcmx_gcc_ld_script

add_project_link_arguments(startup_ld_arg, language : 'c')
