project('tplxv2-gifdec', ['c', 'cpp'],
	version : '0.0.2',
	default_options : [
	'cpp_std=c++17']
	)

project_description = 'gifdec with minor fixes, build with meson, for C++ & coreboot payload usage'

add_project_arguments(
	['-xc++'], language: 'c'
)

cpp = meson.get_compiler('cpp')

gifdec_src = ['gifdec.c']
gifdec_example_src = ['example.c']
gifdec_h = ['gifdec.h']

gifdec_incdir = include_directories('.')
gifdec_lib = static_library('gifdecpp',
	gifdec_src,
	link_language : 'cpp',
	include_directories: '.',
	install : true,
	install_dir : meson.current_source_dir()
	)

gifplay_exec = executable('gifplay',
	gifdec_example_src,
	link_with: gifdec_lib,
	dependencies: [dependency('sdl2')],
	link_language: 'cpp',
	install : true,
	install_dir : meson.current_source_dir()
	)

gifdec_dep = declare_dependency(
	   include_directories : gifdec_incdir,
	   link_with : gifdec_lib)
