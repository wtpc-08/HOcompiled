Respuestas 
1. Escriban qué esperan de cada uno de los pasos
2. ¿Qué agregó el preprocesador?
3. Identificar en la rutina de assembler las funciones
4. Explicar qué quieren decir los símbolos que se crean en el objeto
5. ¿En qué se diferencian los símbolos del objeto y del ejecutable?

Respuesta 1
Paso 1
Se encarga de las directivas hashtag, includes y macros para no tener que definir funciones y macros usuales, se ve con las variables extern que las declara aunque todavìa no estèn definidas


Paso 2

Pasa el còdigo de C a assembler
 


Paso 3

Pasa de assembler a binario, con info de los descriptores y tipos de entrada

Paso 4

el linker lo transforma en ejecutable cargando las librerias que necesita y que el sistema operativo lo entienda y lo pueda correr

Respuesta 2
en este caso incluyo el stdio.h
el preprocesador agregó, las posiciones de memoria, los descriptores en mayùsculas si se pueden linkear y ser vistos desde fuera y con minùsculas sino y tipos de entrada

Respuesta 3
los simbolos significan T que es texto, U no està definido se define afuera, r, sòlo se puede leer, d es data etc...


0000000000400569 T add_numbers
0000000000601040 B __bss_start
0000000000601040 b completed.6973
0000000000601030 D __data_start
0000000000601030 W data_start
0000000000400470 t deregister_tm_clones
00000000004004e0 t __do_global_dtors_aux
0000000000600e18 t __do_global_dtors_aux_fini_array_entry
0000000000601038 D __dso_handle
0000000000600e28 d _DYNAMIC
0000000000601040 D _edata
0000000000601048 B _end
00000000004005f4 T _fini
0000000000400500 t frame_dummy
0000000000600e10 t __frame_dummy_init_array_entry
0000000000400778 r __FRAME_END__
0000000000601000 d _GLOBAL_OFFSET_TABLE_
                 w __gmon_start__
00000000004003e0 T _init
0000000000600e18 t __init_array_end
0000000000600e10 t __init_array_start
0000000000400600 R _IO_stdin_used
                 w _ITM_deregisterTMCloneTable
                 w _ITM_registerTMCloneTable
0000000000600e20 d __JCR_END__
0000000000600e20 d __JCR_LIST__
                 w _Jv_RegisterClasses
00000000004005f0 T __libc_csu_fini
0000000000400580 T __libc_csu_init
                 U __libc_start_main@@GLIBC_2.2.5
000000000040052d T main
                 U printf@@GLIBC_2.2.5
00000000004004a0 t register_tm_clones
0000000000400440 T _start
0000000000601040 D __TMC_END__


Respuesta 4

las funciones son  U printf@@GLIBC_2.2.5, U printf@@GLIBC_2.2.5 y add_numbers

