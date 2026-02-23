.
├── AUTHORS.md
├── CONTRIBUTING.md
├── Jenkinsfile
├── LICENSE
├── Makefile
├── README.md
├── configuration
│   ├── checkers.tcl
│   ├── cts.tcl
│   ├── extraction.tcl
│   ├── floorplan.tcl
│   ├── general.tcl
│   ├── load_order.txt
│   ├── placement.tcl
│   ├── routing.tcl
│   └── synthesis.tcl
├── dependencies
│   ├── __pycache__
│   │   └── env_info.cpython-310.pyc
│   ├── arch
│   │   └── run_time.txt
│   ├── centos-7
│   │   ├── compile_time.txt
│   │   ├── precompile_time.txt
│   │   └── run_time.txt
│   ├── env_info.py
│   ├── get_tag.py
│   ├── hash_for.py
│   ├── image_name.mk
│   ├── includedyaml
│   │   ├── LICENSE
│   │   ├── __init__.py
│   │   ├── __pycache__
│   │   │   ├── __init__.cpython-36.pyc
│   │   │   ├── composer.cpython-36.pyc
│   │   │   ├── constructor.cpython-36.pyc
│   │   │   ├── cyaml.cpython-36.pyc
│   │   │   ├── dumper.cpython-36.pyc
│   │   │   ├── emitter.cpython-36.pyc
│   │   │   ├── error.cpython-36.pyc
│   │   │   ├── events.cpython-36.pyc
│   │   │   ├── loader.cpython-36.pyc
│   │   │   ├── nodes.cpython-36.pyc
│   │   │   ├── parser.cpython-36.pyc
│   │   │   ├── reader.cpython-36.pyc
│   │   │   ├── representer.cpython-36.pyc
│   │   │   ├── resolver.cpython-36.pyc
│   │   │   ├── scanner.cpython-36.pyc
│   │   │   ├── serializer.cpython-36.pyc
│   │   │   └── tokens.cpython-36.pyc
│   │   ├── composer.py
│   │   ├── constructor.py
│   │   ├── cyaml.py
│   │   ├── dumper.py
│   │   ├── emitter.py
│   │   ├── error.py
│   │   ├── events.py
│   │   ├── loader.py
│   │   ├── nodes.py
│   │   ├── parser.py
│   │   ├── reader.py
│   │   ├── representer.py
│   │   ├── resolver.py
│   │   ├── scanner.py
│   │   ├── serializer.py
│   │   └── tokens.py
│   ├── macos
│   │   └── run_time.txt
│   ├── python
│   │   ├── compile_time.txt
│   │   ├── precompile_time.txt
│   │   └── run_time.txt
│   ├── tool.py
│   ├── tool_metadata.yml
│   ├── ubuntu-20.04
│   │   └── run_time.txt
│   ├── update_pyyaml.sh
│   ├── verify_versions.py
│   └── version.py
├── designs
│   ├── ci
│   ├── picorv32a
│   │   ├── config.tcl
│   │   ├── runs
│   │   │   └── RUN_2026.02.23_14.06.07
│   │   │       ├── OPENLANE_COMMIT
│   │   │       ├── PDK_SOURCES
│   │   │       ├── cmds.log
│   │   │       ├── config.tcl
│   │   │       ├── config_in.tcl
│   │   │       ├── logs
│   │   │       │   ├── cts
│   │   │       │   ├── floorplan
│   │   │       │   ├── placement
│   │   │       │   ├── routing
│   │   │       │   ├── signoff
│   │   │       │   └── synthesis
│   │   │       │       ├── 1-synthesis.errors
│   │   │       │       ├── 1-synthesis.log
│   │   │       │       ├── 1-synthesis.warnings
│   │   │       │       ├── 2-sta.errors
│   │   │       │       ├── 2-sta.log
│   │   │       │       └── 2-sta.warnings
│   │   │       ├── openlane.log
│   │   │       ├── reports
│   │   │       │   ├── cts
│   │   │       │   ├── floorplan
│   │   │       │   ├── placement
│   │   │       │   ├── routing
│   │   │       │   ├── signoff
│   │   │       │   └── synthesis
│   │   │       │       ├── 1-synthesis.AREA_0.chk.rpt
│   │   │       │       ├── 1-synthesis.AREA_0.stat.rpt
│   │   │       │       ├── 1-synthesis_dff.stat
│   │   │       │       ├── 1-synthesis_pre.stat
│   │   │       │       └── 1-synthesis_pre_synth.chk.rpt
│   │   │       ├── results
│   │   │       │   ├── cts
│   │   │       │   ├── floorplan
│   │   │       │   ├── placement
│   │   │       │   ├── routing
│   │   │       │   ├── signoff
│   │   │       │   └── synthesis
│   │   │       │       ├── picorv32a.sdf
│   │   │       │       └── picorv32a.v
│   │   │       ├── runtime.yaml
│   │   │       └── tmp
│   │   │           ├── cts
│   │   │           │   ├── cts-fastest.lib
│   │   │           │   ├── cts-fastest.lib.exclude.list
│   │   │           │   ├── cts-slowest.lib
│   │   │           │   ├── cts-slowest.lib.exclude.list
│   │   │           │   ├── cts.lib
│   │   │           │   └── cts.lib.exclude.list
│   │   │           ├── floorplan
│   │   │           ├── layers.list
│   │   │           ├── merged.max.lef
│   │   │           ├── merged.min.lef
│   │   │           ├── merged.nom.lef
│   │   │           ├── placement
│   │   │           ├── routing
│   │   │           │   └── config.tracks
│   │   │           ├── signoff
│   │   │           └── synthesis
│   │   │               ├── 1-sky130_fd_sc_hd__tt_025C_1v80.no_pg.lib
│   │   │               ├── 1-trimmed.no_pg.lib
│   │   │               ├── hierarchy.dot
│   │   │               ├── merged.lib
│   │   │               ├── post_techmap.dot
│   │   │               ├── synthesis.sdc
│   │   │               ├── trimmed.lib
│   │   │               └── trimmed.lib.exclude.list
│   │   └── src
│   │       ├── picorv32a.sdc
│   │       └── picorv32a.v
│   └── spm
│       ├── config.json
│       ├── pin_order.cfg
│       └── src
│           ├── spm.sdc
│           └── spm.v
├── docker
│   ├── Makefile
│   ├── README.md
│   ├── build_base
│   │   └── Dockerfile
│   ├── current_platform.py
│   ├── cvc_rv
│   │   └── Dockerfile
│   ├── git
│   │   └── Dockerfile
│   ├── klayout
│   │   ├── Dockerfile
│   │   └── build_klayout.sh
│   ├── magic
│   │   └── Dockerfile
│   ├── netgen
│   │   └── Dockerfile
│   ├── openlane
│   │   └── Dockerfile.tpl
│   ├── openroad_app
│   │   └── Dockerfile
│   ├── padring
│   │   └── Dockerfile
│   ├── run_base
│   │   └── Dockerfile
│   ├── tar
│   ├── utils.py
│   ├── verilator
│   │   └── Dockerfile
│   ├── vlogtoverilog
│   │   └── Dockerfile
│   └── yosys
│       └── Dockerfile
├── docs
│   ├── Makefile
│   ├── _ext
│   │   ├── image_links.py
│   │   ├── markdown_code_links.py
│   │   ├── markdown_cross_doc_section_links.py
│   │   └── util.py
│   ├── _static
│   │   ├── digital_flow
│   │   │   ├── broken_aspect_ratio.png
│   │   │   ├── final_def.png
│   │   │   ├── final_gds.png
│   │   │   ├── floorplan_def_loaded.png
│   │   │   ├── lvs_issue.png
│   │   │   ├── lvs_issue_comparison.png
│   │   │   ├── mem_1r1w_def.png
│   │   │   └── ring_around_macro.png
│   │   ├── docs_contribution
│   │   │   ├── code_block_issue.png
│   │   │   ├── code_block_spaces_around_the_code.png
│   │   │   └── code_block_supposed_look.png
│   │   ├── eco_flow.png
│   │   ├── eco_results.png
│   │   ├── flow_v1.png
│   │   ├── gha.png
│   │   ├── installation
│   │   │   ├── powershell.png
│   │   │   ├── spm.png
│   │   │   ├── wsl.png
│   │   │   └── wsl_docker_settings.png
│   │   ├── librelane_banner.svg
│   │   ├── openram
│   │   │   ├── basic_fp.png
│   │   │   ├── final.png
│   │   │   ├── floorplan_v2.png
│   │   │   └── pdn_macro_hooks_missing.png
│   │   ├── src
│   │   │   ├── actor.png
│   │   │   ├── flow.dot
│   │   │   ├── lvs_issue_comparison.xcf
│   │   │   └── ring_around_macro.xcf
│   │   └── striVe.jpeg
│   ├── requirements.txt
│   └── source
│       ├── additional_material.md
│       ├── authors.md -> ../../AUTHORS.md
│       ├── conf.py
│       ├── flow_overview.md
│       ├── for_developers
│       │   ├── code_contribution.md -> ../../../CONTRIBUTING.md
│       │   ├── docker.md -> ../../../docker/README.md
│       │   ├── docs_contribution.md
│       │   ├── gha_workflow.md
│       │   ├── index.rst
│       │   ├── issue_regression_tests.md
│       │   ├── pdk_structure.md
│       │   └── using_or_issue.md
│       ├── getting_started
│       │   ├── index.rst
│       │   ├── installation
│       │   │   ├── docker_no_root.md
│       │   │   ├── index.rst
│       │   │   ├── installation_common_section.md
│       │   │   ├── installation_linux.md
│       │   │   ├── installation_local.md
│       │   │   ├── installation_macos.md
│       │   │   ├── installation_overview.md
│       │   │   ├── installation_ubuntu.md
│       │   │   ├── installation_win.md
│       │   │   └── wsl_ubuntu_packages.md
│       │   ├── quickstart.md
│       │   └── updating.md
│       ├── index.rst
│       ├── reference
│       │   ├── cli.md
│       │   ├── configuration.md
│       │   ├── configuration_files.md
│       │   ├── datapoint_definitions.md
│       │   ├── gui.md
│       │   ├── index.rst
│       │   ├── interactive_mode.md
│       │   ├── openlane_commands.md
│       │   └── pdk_configuration.md
│       ├── tutorials
│       │   ├── digital_guide.md
│       │   ├── index.rst
│       │   └── openram.md
│       └── usage
│           ├── advanced_power_grid_control.md
│           ├── chip_integration.md
│           ├── custom_pdk_builds.md
│           ├── designs.md
│           ├── exploration_script.md
│           ├── hardening_macros.md
│           └── index.rst
├── env.py
├── flow.tcl
├── gui.py
├── hier.rpt
├── install
├── klayoutrc
├── regression_results
│   └── benchmark_results
│       └── sky130A
│           └── sky130_fd_sc_hd.csv
├── requirements.txt
├── run_designs.py
├── scripts
│   ├── base.sdc
│   ├── compare_regression_design.py
│   ├── compare_regression_reports.py
│   ├── config
│   │   ├── config.py
│   │   ├── extract_opt_variables.py
│   │   ├── init.py
│   │   ├── migrate.py
│   │   ├── replicate.py
│   │   ├── tcl.py
│   │   └── update.py
│   ├── count_lvs.py
│   ├── drc_rosetta.py
│   ├── extract_antenna_count.py
│   ├── extract_antenna_violators.py
│   ├── generate_reports.py
│   ├── iterate_timing_closure.py
│   ├── klayout
│   │   ├── Readme.md
│   │   ├── open_design.py
│   │   ├── run_drc.sh
│   │   ├── stream_out.py
│   │   └── xor.drc
│   ├── libtrim.py
│   ├── magic
│   │   ├── Readme.md
│   │   ├── def
│   │   │   ├── antenna_check.tcl
│   │   │   ├── mag.tcl
│   │   │   ├── mag_gds.tcl
│   │   │   └── read.tcl
│   │   ├── drc.tcl
│   │   ├── erase_box.sh
│   │   ├── extract_spice.tcl
│   │   ├── gds
│   │   │   ├── drc_batch.tcl
│   │   │   ├── erase_box.tcl
│   │   │   ├── extras_mag.tcl
│   │   │   └── mag_with_pointers.tcl
│   │   ├── lef
│   │   │   ├── extras_maglef.tcl
│   │   │   └── maglef.tcl
│   │   ├── lef.tcl
│   │   └── wrapper.tcl
│   ├── mergeLef.py
│   ├── mergeLib.py
│   ├── most_recent_run.py
│   ├── new_tracks.py
│   ├── odbpy
│   │   ├── __pycache__
│   │   │   └── reader.cpython-36.pyc
│   │   ├── apply_def_template.py
│   │   ├── contextualize.py
│   │   ├── defutil.py
│   │   ├── diodes.py
│   │   ├── io_place.py
│   │   ├── label_macro_pins.py
│   │   ├── lefutil.py
│   │   ├── manual_macro_place.py
│   │   ├── padringer.py
│   │   ├── power_utils.py
│   │   ├── random_place.py
│   │   ├── reader.py
│   │   ├── snap_to_grid.py
│   │   └── wire_lengths.py
│   ├── openlane-1.0.2.tm
│   ├── openlane_utils-1.0.2.tm
│   ├── openroad
│   │   ├── antenna_check.tcl
│   │   ├── basic_mp.tcl
│   │   ├── common
│   │   │   ├── dpl_cell_pad.tcl
│   │   │   ├── io.tcl
│   │   │   ├── pdn_cfg.tcl
│   │   │   ├── resizer.tcl
│   │   │   ├── set_global_connections.tcl
│   │   │   ├── set_layer_adjustments.tcl
│   │   │   ├── set_rc.tcl
│   │   │   └── set_routing_layers.tcl
│   │   ├── cts.tcl
│   │   ├── diodes.tcl
│   │   ├── dpl.tcl
│   │   ├── droute.tcl
│   │   ├── fill.tcl
│   │   ├── floorplan.tcl
│   │   ├── gpl.tcl
│   │   ├── groute.tcl
│   │   ├── gui.tcl
│   │   ├── insert_buffer.tcl
│   │   ├── ioplacer.tcl
│   │   ├── irdrop.tcl
│   │   ├── pdn.tcl
│   │   ├── rcx.tcl
│   │   ├── resizer.tcl
│   │   ├── resizer_routing_design.tcl
│   │   ├── resizer_routing_timing.tcl
│   │   ├── resizer_timing.tcl
│   │   ├── sta
│   │   │   └── multi_corner.tcl
│   │   ├── tapcell.tcl
│   │   └── write_views.tcl
│   ├── or_issue.py
│   ├── padframe_generator.py
│   ├── parse_yosys_check.py
│   ├── pdk_linker.py
│   ├── report
│   │   ├── get_best.py
│   │   ├── get_file_name.py
│   │   └── report.py
│   ├── synth_exp
│   │   ├── analyze.py
│   │   ├── table.css
│   │   └── utils.js
│   ├── tcl_commands
│   │   ├── README.md
│   │   ├── all.tcl
│   │   ├── checkers.tcl
│   │   ├── cts.tcl
│   │   ├── cvc_rv.tcl
│   │   ├── floorplan.tcl
│   │   ├── init_design.tcl
│   │   ├── klayout.tcl
│   │   ├── lvs.tcl
│   │   ├── magic.tcl
│   │   ├── placement.tcl
│   │   ├── routing.tcl
│   │   ├── sta.tcl
│   │   └── synthesis.tcl
│   ├── topModuleGen
│   │   ├── README.md
│   │   └── src
│   │       ├── TopModuleGen.py
│   │       └── padHelper.py
│   ├── utils
│   │   ├── __init__.py
│   │   ├── deflef_utils.tcl
│   │   ├── fake_display_buffer.tcl
│   │   ├── utils.py
│   │   └── utils.tcl
│   ├── write_runtime.py
│   └── yosys
│       ├── elaborate.tcl
│       ├── logic_equiv_check.tcl
│       ├── rewrite_verilog.tcl
│       └── synth.tcl
├── tests
│   ├── 1007
│   │   ├── config.tcl
│   │   ├── hooks
│   │   │   └── post_run.py
│   │   ├── in.def
│   │   └── interactive.tcl
│   ├── 1413
│   │   ├── config.tcl
│   │   ├── hooks
│   │   │   └── post_run.py
│   │   ├── in.def -> ../1007/in.def
│   │   └── interactive.tcl
│   ├── 1506
│   │   ├── config.json
│   │   ├── hooks
│   │   │   └── post_run.py
│   │   ├── interactive.tcl
│   │   └── src
│   │       └── inverter.v
│   ├── 912
│   │   ├── config.tcl
│   │   ├── def_test.def
│   │   ├── issue_regression.py
│   │   └── src
│   │       └── def_test.v
│   ├── Readme.md
│   └── __main__.py
└── venv
    ├── bin
    │   ├── Activate.ps1
    │   ├── activate
    │   ├── activate.csh
    │   ├── activate.fish
    │   ├── ciel
    │   ├── httpx
    │   ├── markdown-it
    │   ├── pcpp
    │   ├── pip
    │   ├── pip3
    │   ├── pip3.10
    │   ├── pygmentize
    │   ├── python -> python3
    │   ├── python3 -> /usr/bin/python3
    │   ├── python3.10 -> python3
    │   └── wheel
    ├── include
    ├── lib
    │   └── python3.10
    │       └── site-packages
    │           ├── LICENSE.txt
    │           ├── __pycache__
    │           │   └── typing_extensions.cpython-310.pyc
    │           ├── _distutils_hack
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   └── override.cpython-310.pyc
    │           │   └── override.py
    │           ├── _yaml
    │           │   ├── __init__.py
    │           │   └── __pycache__
    │           │       └── __init__.cpython-310.pyc
    │           ├── anyio
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── from_thread.cpython-310.pyc
    │           │   │   ├── functools.cpython-310.pyc
    │           │   │   ├── lowlevel.cpython-310.pyc
    │           │   │   ├── pytest_plugin.cpython-310.pyc
    │           │   │   ├── to_interpreter.cpython-310.pyc
    │           │   │   ├── to_process.cpython-310.pyc
    │           │   │   └── to_thread.cpython-310.pyc
    │           │   ├── _backends
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── _asyncio.cpython-310.pyc
    │           │   │   │   └── _trio.cpython-310.pyc
    │           │   │   ├── _asyncio.py
    │           │   │   └── _trio.py
    │           │   ├── _core
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── _asyncio_selector_thread.cpython-310.pyc
    │           │   │   │   ├── _contextmanagers.cpython-310.pyc
    │           │   │   │   ├── _eventloop.cpython-310.pyc
    │           │   │   │   ├── _exceptions.cpython-310.pyc
    │           │   │   │   ├── _fileio.cpython-310.pyc
    │           │   │   │   ├── _resources.cpython-310.pyc
    │           │   │   │   ├── _signals.cpython-310.pyc
    │           │   │   │   ├── _sockets.cpython-310.pyc
    │           │   │   │   ├── _streams.cpython-310.pyc
    │           │   │   │   ├── _subprocesses.cpython-310.pyc
    │           │   │   │   ├── _synchronization.cpython-310.pyc
    │           │   │   │   ├── _tasks.cpython-310.pyc
    │           │   │   │   ├── _tempfile.cpython-310.pyc
    │           │   │   │   ├── _testing.cpython-310.pyc
    │           │   │   │   └── _typedattr.cpython-310.pyc
    │           │   │   ├── _asyncio_selector_thread.py
    │           │   │   ├── _contextmanagers.py
    │           │   │   ├── _eventloop.py
    │           │   │   ├── _exceptions.py
    │           │   │   ├── _fileio.py
    │           │   │   ├── _resources.py
    │           │   │   ├── _signals.py
    │           │   │   ├── _sockets.py
    │           │   │   ├── _streams.py
    │           │   │   ├── _subprocesses.py
    │           │   │   ├── _synchronization.py
    │           │   │   ├── _tasks.py
    │           │   │   ├── _tempfile.py
    │           │   │   ├── _testing.py
    │           │   │   └── _typedattr.py
    │           │   ├── abc
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── _eventloop.cpython-310.pyc
    │           │   │   │   ├── _resources.cpython-310.pyc
    │           │   │   │   ├── _sockets.cpython-310.pyc
    │           │   │   │   ├── _streams.cpython-310.pyc
    │           │   │   │   ├── _subprocesses.cpython-310.pyc
    │           │   │   │   ├── _tasks.cpython-310.pyc
    │           │   │   │   └── _testing.cpython-310.pyc
    │           │   │   ├── _eventloop.py
    │           │   │   ├── _resources.py
    │           │   │   ├── _sockets.py
    │           │   │   ├── _streams.py
    │           │   │   ├── _subprocesses.py
    │           │   │   ├── _tasks.py
    │           │   │   └── _testing.py
    │           │   ├── from_thread.py
    │           │   ├── functools.py
    │           │   ├── lowlevel.py
    │           │   ├── py.typed
    │           │   ├── pytest_plugin.py
    │           │   ├── streams
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── buffered.cpython-310.pyc
    │           │   │   │   ├── file.cpython-310.pyc
    │           │   │   │   ├── memory.cpython-310.pyc
    │           │   │   │   ├── stapled.cpython-310.pyc
    │           │   │   │   ├── text.cpython-310.pyc
    │           │   │   │   └── tls.cpython-310.pyc
    │           │   │   ├── buffered.py
    │           │   │   ├── file.py
    │           │   │   ├── memory.py
    │           │   │   ├── stapled.py
    │           │   │   ├── text.py
    │           │   │   └── tls.py
    │           │   ├── to_interpreter.py
    │           │   ├── to_process.py
    │           │   └── to_thread.py
    │           ├── anyio-4.12.1.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   ├── entry_points.txt
    │           │   ├── licenses
    │           │   │   └── LICENSE
    │           │   └── top_level.txt
    │           ├── certifi
    │           │   ├── __init__.py
    │           │   ├── __main__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── __main__.cpython-310.pyc
    │           │   │   └── core.cpython-310.pyc
    │           │   ├── cacert.pem
    │           │   ├── core.py
    │           │   └── py.typed
    │           ├── certifi-2026.1.4.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   ├── licenses
    │           │   │   └── LICENSE
    │           │   └── top_level.txt
    │           ├── ciel
    │           │   ├── __init__.py
    │           │   ├── __main__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── __main__.cpython-310.pyc
    │           │   │   ├── __version__.cpython-310.pyc
    │           │   │   ├── click_common.cpython-310.pyc
    │           │   │   ├── common.cpython-310.pyc
    │           │   │   ├── families.cpython-310.pyc
    │           │   │   ├── github.cpython-310.pyc
    │           │   │   ├── manage.cpython-310.pyc
    │           │   │   └── source.cpython-310.pyc
    │           │   ├── __version__.py
    │           │   ├── build
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── common.cpython-310.pyc
    │           │   │   │   ├── gf180mcu.cpython-310.pyc
    │           │   │   │   ├── git_multi_clone.cpython-310.pyc
    │           │   │   │   ├── ihp-sg13g2.cpython-310.pyc
    │           │   │   │   └── sky130.cpython-310.pyc
    │           │   │   ├── common.py
    │           │   │   ├── gf180mcu.py
    │           │   │   ├── git_multi_clone.py
    │           │   │   ├── ihp-sg13g2.py
    │           │   │   └── sky130.py
    │           │   ├── click_common.py
    │           │   ├── common.py
    │           │   ├── families.py
    │           │   ├── github.py
    │           │   ├── manage.py
    │           │   ├── py.typed
    │           │   └── source.py
    │           ├── ciel-2.4.0.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── REQUESTED
    │           │   ├── WHEEL
    │           │   └── entry_points.txt
    │           ├── click
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── _compat.cpython-310.pyc
    │           │   │   ├── _termui_impl.cpython-310.pyc
    │           │   │   ├── _textwrap.cpython-310.pyc
    │           │   │   ├── _utils.cpython-310.pyc
    │           │   │   ├── _winconsole.cpython-310.pyc
    │           │   │   ├── core.cpython-310.pyc
    │           │   │   ├── decorators.cpython-310.pyc
    │           │   │   ├── exceptions.cpython-310.pyc
    │           │   │   ├── formatting.cpython-310.pyc
    │           │   │   ├── globals.cpython-310.pyc
    │           │   │   ├── parser.cpython-310.pyc
    │           │   │   ├── shell_completion.cpython-310.pyc
    │           │   │   ├── termui.cpython-310.pyc
    │           │   │   ├── testing.cpython-310.pyc
    │           │   │   ├── types.cpython-310.pyc
    │           │   │   └── utils.cpython-310.pyc
    │           │   ├── _compat.py
    │           │   ├── _termui_impl.py
    │           │   ├── _textwrap.py
    │           │   ├── _utils.py
    │           │   ├── _winconsole.py
    │           │   ├── core.py
    │           │   ├── decorators.py
    │           │   ├── exceptions.py
    │           │   ├── formatting.py
    │           │   ├── globals.py
    │           │   ├── parser.py
    │           │   ├── py.typed
    │           │   ├── shell_completion.py
    │           │   ├── termui.py
    │           │   ├── testing.py
    │           │   ├── types.py
    │           │   └── utils.py
    │           ├── click-8.3.1.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── REQUESTED
    │           │   ├── WHEEL
    │           │   └── licenses
    │           │       └── LICENSE.txt
    │           ├── distutils-precedence.pth
    │           ├── exceptiongroup
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── _catch.cpython-310.pyc
    │           │   │   ├── _exceptions.cpython-310.pyc
    │           │   │   ├── _formatting.cpython-310.pyc
    │           │   │   ├── _suppress.cpython-310.pyc
    │           │   │   └── _version.cpython-310.pyc
    │           │   ├── _catch.py
    │           │   ├── _exceptions.py
    │           │   ├── _formatting.py
    │           │   ├── _suppress.py
    │           │   ├── _version.py
    │           │   └── py.typed
    │           ├── exceptiongroup-1.3.1.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   └── licenses
    │           │       └── LICENSE
    │           ├── h11
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── _abnf.cpython-310.pyc
    │           │   │   ├── _connection.cpython-310.pyc
    │           │   │   ├── _events.cpython-310.pyc
    │           │   │   ├── _headers.cpython-310.pyc
    │           │   │   ├── _readers.cpython-310.pyc
    │           │   │   ├── _receivebuffer.cpython-310.pyc
    │           │   │   ├── _state.cpython-310.pyc
    │           │   │   ├── _util.cpython-310.pyc
    │           │   │   ├── _version.cpython-310.pyc
    │           │   │   └── _writers.cpython-310.pyc
    │           │   ├── _abnf.py
    │           │   ├── _connection.py
    │           │   ├── _events.py
    │           │   ├── _headers.py
    │           │   ├── _readers.py
    │           │   ├── _receivebuffer.py
    │           │   ├── _state.py
    │           │   ├── _util.py
    │           │   ├── _version.py
    │           │   ├── _writers.py
    │           │   └── py.typed
    │           ├── h11-0.16.0.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   ├── licenses
    │           │   │   └── LICENSE.txt
    │           │   └── top_level.txt
    │           ├── httpcore
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── _api.cpython-310.pyc
    │           │   │   ├── _exceptions.cpython-310.pyc
    │           │   │   ├── _models.cpython-310.pyc
    │           │   │   ├── _ssl.cpython-310.pyc
    │           │   │   ├── _synchronization.cpython-310.pyc
    │           │   │   ├── _trace.cpython-310.pyc
    │           │   │   └── _utils.cpython-310.pyc
    │           │   ├── _api.py
    │           │   ├── _async
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── connection.cpython-310.pyc
    │           │   │   │   ├── connection_pool.cpython-310.pyc
    │           │   │   │   ├── http11.cpython-310.pyc
    │           │   │   │   ├── http2.cpython-310.pyc
    │           │   │   │   ├── http_proxy.cpython-310.pyc
    │           │   │   │   ├── interfaces.cpython-310.pyc
    │           │   │   │   └── socks_proxy.cpython-310.pyc
    │           │   │   ├── connection.py
    │           │   │   ├── connection_pool.py
    │           │   │   ├── http11.py
    │           │   │   ├── http2.py
    │           │   │   ├── http_proxy.py
    │           │   │   ├── interfaces.py
    │           │   │   └── socks_proxy.py
    │           │   ├── _backends
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── anyio.cpython-310.pyc
    │           │   │   │   ├── auto.cpython-310.pyc
    │           │   │   │   ├── base.cpython-310.pyc
    │           │   │   │   ├── mock.cpython-310.pyc
    │           │   │   │   ├── sync.cpython-310.pyc
    │           │   │   │   └── trio.cpython-310.pyc
    │           │   │   ├── anyio.py
    │           │   │   ├── auto.py
    │           │   │   ├── base.py
    │           │   │   ├── mock.py
    │           │   │   ├── sync.py
    │           │   │   └── trio.py
    │           │   ├── _exceptions.py
    │           │   ├── _models.py
    │           │   ├── _ssl.py
    │           │   ├── _sync
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── connection.cpython-310.pyc
    │           │   │   │   ├── connection_pool.cpython-310.pyc
    │           │   │   │   ├── http11.cpython-310.pyc
    │           │   │   │   ├── http2.cpython-310.pyc
    │           │   │   │   ├── http_proxy.cpython-310.pyc
    │           │   │   │   ├── interfaces.cpython-310.pyc
    │           │   │   │   └── socks_proxy.cpython-310.pyc
    │           │   │   ├── connection.py
    │           │   │   ├── connection_pool.py
    │           │   │   ├── http11.py
    │           │   │   ├── http2.py
    │           │   │   ├── http_proxy.py
    │           │   │   ├── interfaces.py
    │           │   │   └── socks_proxy.py
    │           │   ├── _synchronization.py
    │           │   ├── _trace.py
    │           │   ├── _utils.py
    │           │   └── py.typed
    │           ├── httpcore-1.0.9.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   └── licenses
    │           │       └── LICENSE.md
    │           ├── httpx
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── __version__.cpython-310.pyc
    │           │   │   ├── _api.cpython-310.pyc
    │           │   │   ├── _auth.cpython-310.pyc
    │           │   │   ├── _client.cpython-310.pyc
    │           │   │   ├── _config.cpython-310.pyc
    │           │   │   ├── _content.cpython-310.pyc
    │           │   │   ├── _decoders.cpython-310.pyc
    │           │   │   ├── _exceptions.cpython-310.pyc
    │           │   │   ├── _main.cpython-310.pyc
    │           │   │   ├── _models.cpython-310.pyc
    │           │   │   ├── _multipart.cpython-310.pyc
    │           │   │   ├── _status_codes.cpython-310.pyc
    │           │   │   ├── _types.cpython-310.pyc
    │           │   │   ├── _urlparse.cpython-310.pyc
    │           │   │   ├── _urls.cpython-310.pyc
    │           │   │   └── _utils.cpython-310.pyc
    │           │   ├── __version__.py
    │           │   ├── _api.py
    │           │   ├── _auth.py
    │           │   ├── _client.py
    │           │   ├── _config.py
    │           │   ├── _content.py
    │           │   ├── _decoders.py
    │           │   ├── _exceptions.py
    │           │   ├── _main.py
    │           │   ├── _models.py
    │           │   ├── _multipart.py
    │           │   ├── _status_codes.py
    │           │   ├── _transports
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── asgi.cpython-310.pyc
    │           │   │   │   ├── base.cpython-310.pyc
    │           │   │   │   ├── default.cpython-310.pyc
    │           │   │   │   ├── mock.cpython-310.pyc
    │           │   │   │   └── wsgi.cpython-310.pyc
    │           │   │   ├── asgi.py
    │           │   │   ├── base.py
    │           │   │   ├── default.py
    │           │   │   ├── mock.py
    │           │   │   └── wsgi.py
    │           │   ├── _types.py
    │           │   ├── _urlparse.py
    │           │   ├── _urls.py
    │           │   ├── _utils.py
    │           │   └── py.typed
    │           ├── httpx-0.28.1.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   ├── entry_points.txt
    │           │   └── licenses
    │           │       └── LICENSE.md
    │           ├── idna
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── codec.cpython-310.pyc
    │           │   │   ├── compat.cpython-310.pyc
    │           │   │   ├── core.cpython-310.pyc
    │           │   │   ├── idnadata.cpython-310.pyc
    │           │   │   ├── intranges.cpython-310.pyc
    │           │   │   ├── package_data.cpython-310.pyc
    │           │   │   └── uts46data.cpython-310.pyc
    │           │   ├── codec.py
    │           │   ├── compat.py
    │           │   ├── core.py
    │           │   ├── idnadata.py
    │           │   ├── intranges.py
    │           │   ├── package_data.py
    │           │   ├── py.typed
    │           │   └── uts46data.py
    │           ├── idna-3.11.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   └── licenses
    │           │       └── LICENSE.md
    │           ├── markdown_it
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── _compat.cpython-310.pyc
    │           │   │   ├── _punycode.cpython-310.pyc
    │           │   │   ├── main.cpython-310.pyc
    │           │   │   ├── parser_block.cpython-310.pyc
    │           │   │   ├── parser_core.cpython-310.pyc
    │           │   │   ├── parser_inline.cpython-310.pyc
    │           │   │   ├── renderer.cpython-310.pyc
    │           │   │   ├── ruler.cpython-310.pyc
    │           │   │   ├── token.cpython-310.pyc
    │           │   │   ├── tree.cpython-310.pyc
    │           │   │   └── utils.cpython-310.pyc
    │           │   ├── _compat.py
    │           │   ├── _punycode.py
    │           │   ├── cli
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   └── parse.cpython-310.pyc
    │           │   │   └── parse.py
    │           │   ├── common
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── entities.cpython-310.pyc
    │           │   │   │   ├── html_blocks.cpython-310.pyc
    │           │   │   │   ├── html_re.cpython-310.pyc
    │           │   │   │   ├── normalize_url.cpython-310.pyc
    │           │   │   │   └── utils.cpython-310.pyc
    │           │   │   ├── entities.py
    │           │   │   ├── html_blocks.py
    │           │   │   ├── html_re.py
    │           │   │   ├── normalize_url.py
    │           │   │   └── utils.py
    │           │   ├── helpers
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── parse_link_destination.cpython-310.pyc
    │           │   │   │   ├── parse_link_label.cpython-310.pyc
    │           │   │   │   └── parse_link_title.cpython-310.pyc
    │           │   │   ├── parse_link_destination.py
    │           │   │   ├── parse_link_label.py
    │           │   │   └── parse_link_title.py
    │           │   ├── main.py
    │           │   ├── parser_block.py
    │           │   ├── parser_core.py
    │           │   ├── parser_inline.py
    │           │   ├── port.yaml
    │           │   ├── presets
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── commonmark.cpython-310.pyc
    │           │   │   │   ├── default.cpython-310.pyc
    │           │   │   │   └── zero.cpython-310.pyc
    │           │   │   ├── commonmark.py
    │           │   │   ├── default.py
    │           │   │   └── zero.py
    │           │   ├── py.typed
    │           │   ├── renderer.py
    │           │   ├── ruler.py
    │           │   ├── rules_block
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── blockquote.cpython-310.pyc
    │           │   │   │   ├── code.cpython-310.pyc
    │           │   │   │   ├── fence.cpython-310.pyc
    │           │   │   │   ├── heading.cpython-310.pyc
    │           │   │   │   ├── hr.cpython-310.pyc
    │           │   │   │   ├── html_block.cpython-310.pyc
    │           │   │   │   ├── lheading.cpython-310.pyc
    │           │   │   │   ├── list.cpython-310.pyc
    │           │   │   │   ├── paragraph.cpython-310.pyc
    │           │   │   │   ├── reference.cpython-310.pyc
    │           │   │   │   ├── state_block.cpython-310.pyc
    │           │   │   │   └── table.cpython-310.pyc
    │           │   │   ├── blockquote.py
    │           │   │   ├── code.py
    │           │   │   ├── fence.py
    │           │   │   ├── heading.py
    │           │   │   ├── hr.py
    │           │   │   ├── html_block.py
    │           │   │   ├── lheading.py
    │           │   │   ├── list.py
    │           │   │   ├── paragraph.py
    │           │   │   ├── reference.py
    │           │   │   ├── state_block.py
    │           │   │   └── table.py
    │           │   ├── rules_core
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── block.cpython-310.pyc
    │           │   │   │   ├── inline.cpython-310.pyc
    │           │   │   │   ├── linkify.cpython-310.pyc
    │           │   │   │   ├── normalize.cpython-310.pyc
    │           │   │   │   ├── replacements.cpython-310.pyc
    │           │   │   │   ├── smartquotes.cpython-310.pyc
    │           │   │   │   ├── state_core.cpython-310.pyc
    │           │   │   │   └── text_join.cpython-310.pyc
    │           │   │   ├── block.py
    │           │   │   ├── inline.py
    │           │   │   ├── linkify.py
    │           │   │   ├── normalize.py
    │           │   │   ├── replacements.py
    │           │   │   ├── smartquotes.py
    │           │   │   ├── state_core.py
    │           │   │   └── text_join.py
    │           │   ├── rules_inline
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── autolink.cpython-310.pyc
    │           │   │   │   ├── backticks.cpython-310.pyc
    │           │   │   │   ├── balance_pairs.cpython-310.pyc
    │           │   │   │   ├── emphasis.cpython-310.pyc
    │           │   │   │   ├── entity.cpython-310.pyc
    │           │   │   │   ├── escape.cpython-310.pyc
    │           │   │   │   ├── fragments_join.cpython-310.pyc
    │           │   │   │   ├── html_inline.cpython-310.pyc
    │           │   │   │   ├── image.cpython-310.pyc
    │           │   │   │   ├── link.cpython-310.pyc
    │           │   │   │   ├── linkify.cpython-310.pyc
    │           │   │   │   ├── newline.cpython-310.pyc
    │           │   │   │   ├── state_inline.cpython-310.pyc
    │           │   │   │   ├── strikethrough.cpython-310.pyc
    │           │   │   │   └── text.cpython-310.pyc
    │           │   │   ├── autolink.py
    │           │   │   ├── backticks.py
    │           │   │   ├── balance_pairs.py
    │           │   │   ├── emphasis.py
    │           │   │   ├── entity.py
    │           │   │   ├── escape.py
    │           │   │   ├── fragments_join.py
    │           │   │   ├── html_inline.py
    │           │   │   ├── image.py
    │           │   │   ├── link.py
    │           │   │   ├── linkify.py
    │           │   │   ├── newline.py
    │           │   │   ├── state_inline.py
    │           │   │   ├── strikethrough.py
    │           │   │   └── text.py
    │           │   ├── token.py
    │           │   ├── tree.py
    │           │   └── utils.py
    │           ├── markdown_it_py-4.0.0.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   ├── entry_points.txt
    │           │   └── licenses
    │           │       ├── LICENSE
    │           │       └── LICENSE.markdown-it
    │           ├── mdurl
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── _decode.cpython-310.pyc
    │           │   │   ├── _encode.cpython-310.pyc
    │           │   │   ├── _format.cpython-310.pyc
    │           │   │   ├── _parse.cpython-310.pyc
    │           │   │   └── _url.cpython-310.pyc
    │           │   ├── _decode.py
    │           │   ├── _encode.py
    │           │   ├── _format.py
    │           │   ├── _parse.py
    │           │   ├── _url.py
    │           │   └── py.typed
    │           ├── mdurl-0.1.2.dist-info
    │           │   ├── INSTALLER
    │           │   ├── LICENSE
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   └── WHEEL
    │           ├── packaging
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── _elffile.cpython-310.pyc
    │           │   │   ├── _manylinux.cpython-310.pyc
    │           │   │   ├── _musllinux.cpython-310.pyc
    │           │   │   ├── _parser.cpython-310.pyc
    │           │   │   ├── _structures.cpython-310.pyc
    │           │   │   ├── _tokenizer.cpython-310.pyc
    │           │   │   ├── markers.cpython-310.pyc
    │           │   │   ├── metadata.cpython-310.pyc
    │           │   │   ├── pylock.cpython-310.pyc
    │           │   │   ├── requirements.cpython-310.pyc
    │           │   │   ├── specifiers.cpython-310.pyc
    │           │   │   ├── tags.cpython-310.pyc
    │           │   │   ├── utils.cpython-310.pyc
    │           │   │   └── version.cpython-310.pyc
    │           │   ├── _elffile.py
    │           │   ├── _manylinux.py
    │           │   ├── _musllinux.py
    │           │   ├── _parser.py
    │           │   ├── _structures.py
    │           │   ├── _tokenizer.py
    │           │   ├── licenses
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   └── _spdx.cpython-310.pyc
    │           │   │   └── _spdx.py
    │           │   ├── markers.py
    │           │   ├── metadata.py
    │           │   ├── py.typed
    │           │   ├── pylock.py
    │           │   ├── requirements.py
    │           │   ├── specifiers.py
    │           │   ├── tags.py
    │           │   ├── utils.py
    │           │   └── version.py
    │           ├── packaging-26.0.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   └── licenses
    │           │       ├── LICENSE
    │           │       ├── LICENSE.APACHE
    │           │       └── LICENSE.BSD
    │           ├── pcpp
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── evaluator.cpython-310.pyc
    │           │   │   ├── lextab.cpython-310.pyc
    │           │   │   ├── parser.cpython-310.pyc
    │           │   │   ├── parsetab.cpython-310.pyc
    │           │   │   ├── pcmd.cpython-310.pyc
    │           │   │   └── preprocessor.cpython-310.pyc
    │           │   ├── evaluator.py
    │           │   ├── lextab.py
    │           │   ├── parser.py
    │           │   ├── parsetab.py
    │           │   ├── pcmd.py
    │           │   ├── ply
    │           │   │   └── ply
    │           │   │       ├── __init__.py
    │           │   │       ├── __pycache__
    │           │   │       │   ├── __init__.cpython-310.pyc
    │           │   │       │   ├── cpp.cpython-310.pyc
    │           │   │       │   ├── ctokens.cpython-310.pyc
    │           │   │       │   ├── lex.cpython-310.pyc
    │           │   │       │   ├── yacc.cpython-310.pyc
    │           │   │       │   └── ygen.cpython-310.pyc
    │           │   │       ├── cpp.py
    │           │   │       ├── ctokens.py
    │           │   │       ├── lex.py
    │           │   │       ├── yacc.py
    │           │   │       └── ygen.py
    │           │   └── preprocessor.py
    │           ├── pcpp-1.30.dist-info
    │           │   ├── INSTALLER
    │           │   ├── LICENSE.txt
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   ├── entry_points.txt
    │           │   └── top_level.txt
    │           ├── pip
    │           │   ├── __init__.py
    │           │   ├── __main__.py
    │           │   ├── __pip-runner__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── __main__.cpython-310.pyc
    │           │   │   └── __pip-runner__.cpython-310.pyc
    │           │   ├── _internal
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── build_env.cpython-310.pyc
    │           │   │   │   ├── cache.cpython-310.pyc
    │           │   │   │   ├── configuration.cpython-310.pyc
    │           │   │   │   ├── exceptions.cpython-310.pyc
    │           │   │   │   ├── main.cpython-310.pyc
    │           │   │   │   ├── pyproject.cpython-310.pyc
    │           │   │   │   ├── self_outdated_check.cpython-310.pyc
    │           │   │   │   └── wheel_builder.cpython-310.pyc
    │           │   │   ├── build_env.py
    │           │   │   ├── cache.py
    │           │   │   ├── cli
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── autocompletion.cpython-310.pyc
    │           │   │   │   │   ├── base_command.cpython-310.pyc
    │           │   │   │   │   ├── cmdoptions.cpython-310.pyc
    │           │   │   │   │   ├── command_context.cpython-310.pyc
    │           │   │   │   │   ├── index_command.cpython-310.pyc
    │           │   │   │   │   ├── main.cpython-310.pyc
    │           │   │   │   │   ├── main_parser.cpython-310.pyc
    │           │   │   │   │   ├── parser.cpython-310.pyc
    │           │   │   │   │   ├── progress_bars.cpython-310.pyc
    │           │   │   │   │   ├── req_command.cpython-310.pyc
    │           │   │   │   │   ├── spinners.cpython-310.pyc
    │           │   │   │   │   └── status_codes.cpython-310.pyc
    │           │   │   │   ├── autocompletion.py
    │           │   │   │   ├── base_command.py
    │           │   │   │   ├── cmdoptions.py
    │           │   │   │   ├── command_context.py
    │           │   │   │   ├── index_command.py
    │           │   │   │   ├── main.py
    │           │   │   │   ├── main_parser.py
    │           │   │   │   ├── parser.py
    │           │   │   │   ├── progress_bars.py
    │           │   │   │   ├── req_command.py
    │           │   │   │   ├── spinners.py
    │           │   │   │   └── status_codes.py
    │           │   │   ├── commands
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── cache.cpython-310.pyc
    │           │   │   │   │   ├── check.cpython-310.pyc
    │           │   │   │   │   ├── completion.cpython-310.pyc
    │           │   │   │   │   ├── configuration.cpython-310.pyc
    │           │   │   │   │   ├── debug.cpython-310.pyc
    │           │   │   │   │   ├── download.cpython-310.pyc
    │           │   │   │   │   ├── freeze.cpython-310.pyc
    │           │   │   │   │   ├── hash.cpython-310.pyc
    │           │   │   │   │   ├── help.cpython-310.pyc
    │           │   │   │   │   ├── index.cpython-310.pyc
    │           │   │   │   │   ├── inspect.cpython-310.pyc
    │           │   │   │   │   ├── install.cpython-310.pyc
    │           │   │   │   │   ├── list.cpython-310.pyc
    │           │   │   │   │   ├── lock.cpython-310.pyc
    │           │   │   │   │   ├── search.cpython-310.pyc
    │           │   │   │   │   ├── show.cpython-310.pyc
    │           │   │   │   │   ├── uninstall.cpython-310.pyc
    │           │   │   │   │   └── wheel.cpython-310.pyc
    │           │   │   │   ├── cache.py
    │           │   │   │   ├── check.py
    │           │   │   │   ├── completion.py
    │           │   │   │   ├── configuration.py
    │           │   │   │   ├── debug.py
    │           │   │   │   ├── download.py
    │           │   │   │   ├── freeze.py
    │           │   │   │   ├── hash.py
    │           │   │   │   ├── help.py
    │           │   │   │   ├── index.py
    │           │   │   │   ├── inspect.py
    │           │   │   │   ├── install.py
    │           │   │   │   ├── list.py
    │           │   │   │   ├── lock.py
    │           │   │   │   ├── search.py
    │           │   │   │   ├── show.py
    │           │   │   │   ├── uninstall.py
    │           │   │   │   └── wheel.py
    │           │   │   ├── configuration.py
    │           │   │   ├── distributions
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── base.cpython-310.pyc
    │           │   │   │   │   ├── installed.cpython-310.pyc
    │           │   │   │   │   ├── sdist.cpython-310.pyc
    │           │   │   │   │   └── wheel.cpython-310.pyc
    │           │   │   │   ├── base.py
    │           │   │   │   ├── installed.py
    │           │   │   │   ├── sdist.py
    │           │   │   │   └── wheel.py
    │           │   │   ├── exceptions.py
    │           │   │   ├── index
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── collector.cpython-310.pyc
    │           │   │   │   │   ├── package_finder.cpython-310.pyc
    │           │   │   │   │   └── sources.cpython-310.pyc
    │           │   │   │   ├── collector.py
    │           │   │   │   ├── package_finder.py
    │           │   │   │   └── sources.py
    │           │   │   ├── locations
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── _distutils.cpython-310.pyc
    │           │   │   │   │   ├── _sysconfig.cpython-310.pyc
    │           │   │   │   │   └── base.cpython-310.pyc
    │           │   │   │   ├── _distutils.py
    │           │   │   │   ├── _sysconfig.py
    │           │   │   │   └── base.py
    │           │   │   ├── main.py
    │           │   │   ├── metadata
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── _json.cpython-310.pyc
    │           │   │   │   │   ├── base.cpython-310.pyc
    │           │   │   │   │   └── pkg_resources.cpython-310.pyc
    │           │   │   │   ├── _json.py
    │           │   │   │   ├── base.py
    │           │   │   │   ├── importlib
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   ├── _compat.cpython-310.pyc
    │           │   │   │   │   │   ├── _dists.cpython-310.pyc
    │           │   │   │   │   │   └── _envs.cpython-310.pyc
    │           │   │   │   │   ├── _compat.py
    │           │   │   │   │   ├── _dists.py
    │           │   │   │   │   └── _envs.py
    │           │   │   │   └── pkg_resources.py
    │           │   │   ├── models
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── candidate.cpython-310.pyc
    │           │   │   │   │   ├── direct_url.cpython-310.pyc
    │           │   │   │   │   ├── format_control.cpython-310.pyc
    │           │   │   │   │   ├── index.cpython-310.pyc
    │           │   │   │   │   ├── installation_report.cpython-310.pyc
    │           │   │   │   │   ├── link.cpython-310.pyc
    │           │   │   │   │   ├── release_control.cpython-310.pyc
    │           │   │   │   │   ├── scheme.cpython-310.pyc
    │           │   │   │   │   ├── search_scope.cpython-310.pyc
    │           │   │   │   │   ├── selection_prefs.cpython-310.pyc
    │           │   │   │   │   ├── target_python.cpython-310.pyc
    │           │   │   │   │   └── wheel.cpython-310.pyc
    │           │   │   │   ├── candidate.py
    │           │   │   │   ├── direct_url.py
    │           │   │   │   ├── format_control.py
    │           │   │   │   ├── index.py
    │           │   │   │   ├── installation_report.py
    │           │   │   │   ├── link.py
    │           │   │   │   ├── release_control.py
    │           │   │   │   ├── scheme.py
    │           │   │   │   ├── search_scope.py
    │           │   │   │   ├── selection_prefs.py
    │           │   │   │   ├── target_python.py
    │           │   │   │   └── wheel.py
    │           │   │   ├── network
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── auth.cpython-310.pyc
    │           │   │   │   │   ├── cache.cpython-310.pyc
    │           │   │   │   │   ├── download.cpython-310.pyc
    │           │   │   │   │   ├── lazy_wheel.cpython-310.pyc
    │           │   │   │   │   ├── session.cpython-310.pyc
    │           │   │   │   │   ├── utils.cpython-310.pyc
    │           │   │   │   │   └── xmlrpc.cpython-310.pyc
    │           │   │   │   ├── auth.py
    │           │   │   │   ├── cache.py
    │           │   │   │   ├── download.py
    │           │   │   │   ├── lazy_wheel.py
    │           │   │   │   ├── session.py
    │           │   │   │   ├── utils.py
    │           │   │   │   └── xmlrpc.py
    │           │   │   ├── operations
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── check.cpython-310.pyc
    │           │   │   │   │   ├── freeze.cpython-310.pyc
    │           │   │   │   │   └── prepare.cpython-310.pyc
    │           │   │   │   ├── build
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   ├── build_tracker.cpython-310.pyc
    │           │   │   │   │   │   ├── metadata.cpython-310.pyc
    │           │   │   │   │   │   ├── metadata_editable.cpython-310.pyc
    │           │   │   │   │   │   ├── wheel.cpython-310.pyc
    │           │   │   │   │   │   └── wheel_editable.cpython-310.pyc
    │           │   │   │   │   ├── build_tracker.py
    │           │   │   │   │   ├── metadata.py
    │           │   │   │   │   ├── metadata_editable.py
    │           │   │   │   │   ├── wheel.py
    │           │   │   │   │   └── wheel_editable.py
    │           │   │   │   ├── check.py
    │           │   │   │   ├── freeze.py
    │           │   │   │   ├── install
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   └── wheel.cpython-310.pyc
    │           │   │   │   │   └── wheel.py
    │           │   │   │   └── prepare.py
    │           │   │   ├── pyproject.py
    │           │   │   ├── req
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── constructors.cpython-310.pyc
    │           │   │   │   │   ├── pep723.cpython-310.pyc
    │           │   │   │   │   ├── req_dependency_group.cpython-310.pyc
    │           │   │   │   │   ├── req_file.cpython-310.pyc
    │           │   │   │   │   ├── req_install.cpython-310.pyc
    │           │   │   │   │   ├── req_set.cpython-310.pyc
    │           │   │   │   │   └── req_uninstall.cpython-310.pyc
    │           │   │   │   ├── constructors.py
    │           │   │   │   ├── pep723.py
    │           │   │   │   ├── req_dependency_group.py
    │           │   │   │   ├── req_file.py
    │           │   │   │   ├── req_install.py
    │           │   │   │   ├── req_set.py
    │           │   │   │   └── req_uninstall.py
    │           │   │   ├── resolution
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   └── base.cpython-310.pyc
    │           │   │   │   ├── base.py
    │           │   │   │   ├── legacy
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   └── resolver.cpython-310.pyc
    │           │   │   │   │   └── resolver.py
    │           │   │   │   └── resolvelib
    │           │   │   │       ├── __init__.py
    │           │   │   │       ├── __pycache__
    │           │   │   │       │   ├── __init__.cpython-310.pyc
    │           │   │   │       │   ├── base.cpython-310.pyc
    │           │   │   │       │   ├── candidates.cpython-310.pyc
    │           │   │   │       │   ├── factory.cpython-310.pyc
    │           │   │   │       │   ├── found_candidates.cpython-310.pyc
    │           │   │   │       │   ├── provider.cpython-310.pyc
    │           │   │   │       │   ├── reporter.cpython-310.pyc
    │           │   │   │       │   ├── requirements.cpython-310.pyc
    │           │   │   │       │   └── resolver.cpython-310.pyc
    │           │   │   │       ├── base.py
    │           │   │   │       ├── candidates.py
    │           │   │   │       ├── factory.py
    │           │   │   │       ├── found_candidates.py
    │           │   │   │       ├── provider.py
    │           │   │   │       ├── reporter.py
    │           │   │   │       ├── requirements.py
    │           │   │   │       └── resolver.py
    │           │   │   ├── self_outdated_check.py
    │           │   │   ├── utils
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── _jaraco_text.cpython-310.pyc
    │           │   │   │   │   ├── _log.cpython-310.pyc
    │           │   │   │   │   ├── appdirs.cpython-310.pyc
    │           │   │   │   │   ├── compat.cpython-310.pyc
    │           │   │   │   │   ├── compatibility_tags.cpython-310.pyc
    │           │   │   │   │   ├── datetime.cpython-310.pyc
    │           │   │   │   │   ├── deprecation.cpython-310.pyc
    │           │   │   │   │   ├── direct_url_helpers.cpython-310.pyc
    │           │   │   │   │   ├── egg_link.cpython-310.pyc
    │           │   │   │   │   ├── entrypoints.cpython-310.pyc
    │           │   │   │   │   ├── filesystem.cpython-310.pyc
    │           │   │   │   │   ├── filetypes.cpython-310.pyc
    │           │   │   │   │   ├── glibc.cpython-310.pyc
    │           │   │   │   │   ├── hashes.cpython-310.pyc
    │           │   │   │   │   ├── logging.cpython-310.pyc
    │           │   │   │   │   ├── misc.cpython-310.pyc
    │           │   │   │   │   ├── packaging.cpython-310.pyc
    │           │   │   │   │   ├── pylock.cpython-310.pyc
    │           │   │   │   │   ├── retry.cpython-310.pyc
    │           │   │   │   │   ├── subprocess.cpython-310.pyc
    │           │   │   │   │   ├── temp_dir.cpython-310.pyc
    │           │   │   │   │   ├── unpacking.cpython-310.pyc
    │           │   │   │   │   ├── urls.cpython-310.pyc
    │           │   │   │   │   ├── virtualenv.cpython-310.pyc
    │           │   │   │   │   └── wheel.cpython-310.pyc
    │           │   │   │   ├── _jaraco_text.py
    │           │   │   │   ├── _log.py
    │           │   │   │   ├── appdirs.py
    │           │   │   │   ├── compat.py
    │           │   │   │   ├── compatibility_tags.py
    │           │   │   │   ├── datetime.py
    │           │   │   │   ├── deprecation.py
    │           │   │   │   ├── direct_url_helpers.py
    │           │   │   │   ├── egg_link.py
    │           │   │   │   ├── entrypoints.py
    │           │   │   │   ├── filesystem.py
    │           │   │   │   ├── filetypes.py
    │           │   │   │   ├── glibc.py
    │           │   │   │   ├── hashes.py
    │           │   │   │   ├── logging.py
    │           │   │   │   ├── misc.py
    │           │   │   │   ├── packaging.py
    │           │   │   │   ├── pylock.py
    │           │   │   │   ├── retry.py
    │           │   │   │   ├── subprocess.py
    │           │   │   │   ├── temp_dir.py
    │           │   │   │   ├── unpacking.py
    │           │   │   │   ├── urls.py
    │           │   │   │   ├── virtualenv.py
    │           │   │   │   └── wheel.py
    │           │   │   ├── vcs
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── bazaar.cpython-310.pyc
    │           │   │   │   │   ├── git.cpython-310.pyc
    │           │   │   │   │   ├── mercurial.cpython-310.pyc
    │           │   │   │   │   ├── subversion.cpython-310.pyc
    │           │   │   │   │   └── versioncontrol.cpython-310.pyc
    │           │   │   │   ├── bazaar.py
    │           │   │   │   ├── git.py
    │           │   │   │   ├── mercurial.py
    │           │   │   │   ├── subversion.py
    │           │   │   │   └── versioncontrol.py
    │           │   │   └── wheel_builder.py
    │           │   ├── _vendor
    │           │   │   ├── README.rst
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   └── __init__.cpython-310.pyc
    │           │   │   ├── cachecontrol
    │           │   │   │   ├── LICENSE.txt
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── _cmd.cpython-310.pyc
    │           │   │   │   │   ├── adapter.cpython-310.pyc
    │           │   │   │   │   ├── cache.cpython-310.pyc
    │           │   │   │   │   ├── controller.cpython-310.pyc
    │           │   │   │   │   ├── filewrapper.cpython-310.pyc
    │           │   │   │   │   ├── heuristics.cpython-310.pyc
    │           │   │   │   │   ├── serialize.cpython-310.pyc
    │           │   │   │   │   └── wrapper.cpython-310.pyc
    │           │   │   │   ├── _cmd.py
    │           │   │   │   ├── adapter.py
    │           │   │   │   ├── cache.py
    │           │   │   │   ├── caches
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   ├── file_cache.cpython-310.pyc
    │           │   │   │   │   │   └── redis_cache.cpython-310.pyc
    │           │   │   │   │   ├── file_cache.py
    │           │   │   │   │   └── redis_cache.py
    │           │   │   │   ├── controller.py
    │           │   │   │   ├── filewrapper.py
    │           │   │   │   ├── heuristics.py
    │           │   │   │   ├── py.typed
    │           │   │   │   ├── serialize.py
    │           │   │   │   └── wrapper.py
    │           │   │   ├── certifi
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __main__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── __main__.cpython-310.pyc
    │           │   │   │   │   └── core.cpython-310.pyc
    │           │   │   │   ├── cacert.pem
    │           │   │   │   ├── core.py
    │           │   │   │   └── py.typed
    │           │   │   ├── dependency_groups
    │           │   │   │   ├── LICENSE.txt
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __main__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── __main__.cpython-310.pyc
    │           │   │   │   │   ├── _implementation.cpython-310.pyc
    │           │   │   │   │   ├── _lint_dependency_groups.cpython-310.pyc
    │           │   │   │   │   ├── _pip_wrapper.cpython-310.pyc
    │           │   │   │   │   └── _toml_compat.cpython-310.pyc
    │           │   │   │   ├── _implementation.py
    │           │   │   │   ├── _lint_dependency_groups.py
    │           │   │   │   ├── _pip_wrapper.py
    │           │   │   │   ├── _toml_compat.py
    │           │   │   │   └── py.typed
    │           │   │   ├── distlib
    │           │   │   │   ├── LICENSE.txt
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── compat.cpython-310.pyc
    │           │   │   │   │   ├── resources.cpython-310.pyc
    │           │   │   │   │   ├── scripts.cpython-310.pyc
    │           │   │   │   │   └── util.cpython-310.pyc
    │           │   │   │   ├── compat.py
    │           │   │   │   ├── resources.py
    │           │   │   │   ├── scripts.py
    │           │   │   │   ├── t32.exe
    │           │   │   │   ├── t64-arm.exe
    │           │   │   │   ├── t64.exe
    │           │   │   │   ├── util.py
    │           │   │   │   ├── w32.exe
    │           │   │   │   ├── w64-arm.exe
    │           │   │   │   └── w64.exe
    │           │   │   ├── distro
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __main__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── __main__.cpython-310.pyc
    │           │   │   │   │   └── distro.cpython-310.pyc
    │           │   │   │   ├── distro.py
    │           │   │   │   └── py.typed
    │           │   │   ├── idna
    │           │   │   │   ├── LICENSE.md
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── codec.cpython-310.pyc
    │           │   │   │   │   ├── compat.cpython-310.pyc
    │           │   │   │   │   ├── core.cpython-310.pyc
    │           │   │   │   │   ├── idnadata.cpython-310.pyc
    │           │   │   │   │   ├── intranges.cpython-310.pyc
    │           │   │   │   │   ├── package_data.cpython-310.pyc
    │           │   │   │   │   └── uts46data.cpython-310.pyc
    │           │   │   │   ├── codec.py
    │           │   │   │   ├── compat.py
    │           │   │   │   ├── core.py
    │           │   │   │   ├── idnadata.py
    │           │   │   │   ├── intranges.py
    │           │   │   │   ├── package_data.py
    │           │   │   │   ├── py.typed
    │           │   │   │   └── uts46data.py
    │           │   │   ├── msgpack
    │           │   │   │   ├── COPYING
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── exceptions.cpython-310.pyc
    │           │   │   │   │   ├── ext.cpython-310.pyc
    │           │   │   │   │   └── fallback.cpython-310.pyc
    │           │   │   │   ├── exceptions.py
    │           │   │   │   ├── ext.py
    │           │   │   │   └── fallback.py
    │           │   │   ├── packaging
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── LICENSE.APACHE
    │           │   │   │   ├── LICENSE.BSD
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── _elffile.cpython-310.pyc
    │           │   │   │   │   ├── _manylinux.cpython-310.pyc
    │           │   │   │   │   ├── _musllinux.cpython-310.pyc
    │           │   │   │   │   ├── _parser.cpython-310.pyc
    │           │   │   │   │   ├── _structures.cpython-310.pyc
    │           │   │   │   │   ├── _tokenizer.cpython-310.pyc
    │           │   │   │   │   ├── markers.cpython-310.pyc
    │           │   │   │   │   ├── metadata.cpython-310.pyc
    │           │   │   │   │   ├── pylock.cpython-310.pyc
    │           │   │   │   │   ├── requirements.cpython-310.pyc
    │           │   │   │   │   ├── specifiers.cpython-310.pyc
    │           │   │   │   │   ├── tags.cpython-310.pyc
    │           │   │   │   │   ├── utils.cpython-310.pyc
    │           │   │   │   │   └── version.cpython-310.pyc
    │           │   │   │   ├── _elffile.py
    │           │   │   │   ├── _manylinux.py
    │           │   │   │   ├── _musllinux.py
    │           │   │   │   ├── _parser.py
    │           │   │   │   ├── _structures.py
    │           │   │   │   ├── _tokenizer.py
    │           │   │   │   ├── licenses
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   └── _spdx.cpython-310.pyc
    │           │   │   │   │   └── _spdx.py
    │           │   │   │   ├── markers.py
    │           │   │   │   ├── metadata.py
    │           │   │   │   ├── py.typed
    │           │   │   │   ├── pylock.py
    │           │   │   │   ├── requirements.py
    │           │   │   │   ├── specifiers.py
    │           │   │   │   ├── tags.py
    │           │   │   │   ├── utils.py
    │           │   │   │   └── version.py
    │           │   │   ├── pkg_resources
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── __init__.py
    │           │   │   │   └── __pycache__
    │           │   │   │       └── __init__.cpython-310.pyc
    │           │   │   ├── platformdirs
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __main__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── __main__.cpython-310.pyc
    │           │   │   │   │   ├── android.cpython-310.pyc
    │           │   │   │   │   ├── api.cpython-310.pyc
    │           │   │   │   │   ├── macos.cpython-310.pyc
    │           │   │   │   │   ├── unix.cpython-310.pyc
    │           │   │   │   │   ├── version.cpython-310.pyc
    │           │   │   │   │   └── windows.cpython-310.pyc
    │           │   │   │   ├── android.py
    │           │   │   │   ├── api.py
    │           │   │   │   ├── macos.py
    │           │   │   │   ├── py.typed
    │           │   │   │   ├── unix.py
    │           │   │   │   ├── version.py
    │           │   │   │   └── windows.py
    │           │   │   ├── pygments
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __main__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── __main__.cpython-310.pyc
    │           │   │   │   │   ├── console.cpython-310.pyc
    │           │   │   │   │   ├── filter.cpython-310.pyc
    │           │   │   │   │   ├── formatter.cpython-310.pyc
    │           │   │   │   │   ├── lexer.cpython-310.pyc
    │           │   │   │   │   ├── modeline.cpython-310.pyc
    │           │   │   │   │   ├── plugin.cpython-310.pyc
    │           │   │   │   │   ├── regexopt.cpython-310.pyc
    │           │   │   │   │   ├── scanner.cpython-310.pyc
    │           │   │   │   │   ├── sphinxext.cpython-310.pyc
    │           │   │   │   │   ├── style.cpython-310.pyc
    │           │   │   │   │   ├── token.cpython-310.pyc
    │           │   │   │   │   ├── unistring.cpython-310.pyc
    │           │   │   │   │   └── util.cpython-310.pyc
    │           │   │   │   ├── console.py
    │           │   │   │   ├── filter.py
    │           │   │   │   ├── filters
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   └── __pycache__
    │           │   │   │   │       └── __init__.cpython-310.pyc
    │           │   │   │   ├── formatter.py
    │           │   │   │   ├── formatters
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   └── _mapping.cpython-310.pyc
    │           │   │   │   │   └── _mapping.py
    │           │   │   │   ├── lexer.py
    │           │   │   │   ├── lexers
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   ├── _mapping.cpython-310.pyc
    │           │   │   │   │   │   └── python.cpython-310.pyc
    │           │   │   │   │   ├── _mapping.py
    │           │   │   │   │   └── python.py
    │           │   │   │   ├── modeline.py
    │           │   │   │   ├── plugin.py
    │           │   │   │   ├── regexopt.py
    │           │   │   │   ├── scanner.py
    │           │   │   │   ├── sphinxext.py
    │           │   │   │   ├── style.py
    │           │   │   │   ├── styles
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   └── _mapping.cpython-310.pyc
    │           │   │   │   │   └── _mapping.py
    │           │   │   │   ├── token.py
    │           │   │   │   ├── unistring.py
    │           │   │   │   └── util.py
    │           │   │   ├── pyproject_hooks
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   └── _impl.cpython-310.pyc
    │           │   │   │   ├── _impl.py
    │           │   │   │   ├── _in_process
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   └── _in_process.cpython-310.pyc
    │           │   │   │   │   └── _in_process.py
    │           │   │   │   └── py.typed
    │           │   │   ├── requests
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── __version__.cpython-310.pyc
    │           │   │   │   │   ├── _internal_utils.cpython-310.pyc
    │           │   │   │   │   ├── adapters.cpython-310.pyc
    │           │   │   │   │   ├── api.cpython-310.pyc
    │           │   │   │   │   ├── auth.cpython-310.pyc
    │           │   │   │   │   ├── certs.cpython-310.pyc
    │           │   │   │   │   ├── compat.cpython-310.pyc
    │           │   │   │   │   ├── cookies.cpython-310.pyc
    │           │   │   │   │   ├── exceptions.cpython-310.pyc
    │           │   │   │   │   ├── help.cpython-310.pyc
    │           │   │   │   │   ├── hooks.cpython-310.pyc
    │           │   │   │   │   ├── models.cpython-310.pyc
    │           │   │   │   │   ├── packages.cpython-310.pyc
    │           │   │   │   │   ├── sessions.cpython-310.pyc
    │           │   │   │   │   ├── status_codes.cpython-310.pyc
    │           │   │   │   │   ├── structures.cpython-310.pyc
    │           │   │   │   │   └── utils.cpython-310.pyc
    │           │   │   │   ├── __version__.py
    │           │   │   │   ├── _internal_utils.py
    │           │   │   │   ├── adapters.py
    │           │   │   │   ├── api.py
    │           │   │   │   ├── auth.py
    │           │   │   │   ├── certs.py
    │           │   │   │   ├── compat.py
    │           │   │   │   ├── cookies.py
    │           │   │   │   ├── exceptions.py
    │           │   │   │   ├── help.py
    │           │   │   │   ├── hooks.py
    │           │   │   │   ├── models.py
    │           │   │   │   ├── packages.py
    │           │   │   │   ├── sessions.py
    │           │   │   │   ├── status_codes.py
    │           │   │   │   ├── structures.py
    │           │   │   │   └── utils.py
    │           │   │   ├── resolvelib
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── providers.cpython-310.pyc
    │           │   │   │   │   ├── reporters.cpython-310.pyc
    │           │   │   │   │   └── structs.cpython-310.pyc
    │           │   │   │   ├── providers.py
    │           │   │   │   ├── py.typed
    │           │   │   │   ├── reporters.py
    │           │   │   │   ├── resolvers
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   ├── abstract.cpython-310.pyc
    │           │   │   │   │   │   ├── criterion.cpython-310.pyc
    │           │   │   │   │   │   ├── exceptions.cpython-310.pyc
    │           │   │   │   │   │   └── resolution.cpython-310.pyc
    │           │   │   │   │   ├── abstract.py
    │           │   │   │   │   ├── criterion.py
    │           │   │   │   │   ├── exceptions.py
    │           │   │   │   │   └── resolution.py
    │           │   │   │   └── structs.py
    │           │   │   ├── rich
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __main__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── __main__.cpython-310.pyc
    │           │   │   │   │   ├── _cell_widths.cpython-310.pyc
    │           │   │   │   │   ├── _emoji_codes.cpython-310.pyc
    │           │   │   │   │   ├── _emoji_replace.cpython-310.pyc
    │           │   │   │   │   ├── _export_format.cpython-310.pyc
    │           │   │   │   │   ├── _extension.cpython-310.pyc
    │           │   │   │   │   ├── _fileno.cpython-310.pyc
    │           │   │   │   │   ├── _inspect.cpython-310.pyc
    │           │   │   │   │   ├── _log_render.cpython-310.pyc
    │           │   │   │   │   ├── _loop.cpython-310.pyc
    │           │   │   │   │   ├── _null_file.cpython-310.pyc
    │           │   │   │   │   ├── _palettes.cpython-310.pyc
    │           │   │   │   │   ├── _pick.cpython-310.pyc
    │           │   │   │   │   ├── _ratio.cpython-310.pyc
    │           │   │   │   │   ├── _spinners.cpython-310.pyc
    │           │   │   │   │   ├── _stack.cpython-310.pyc
    │           │   │   │   │   ├── _timer.cpython-310.pyc
    │           │   │   │   │   ├── _win32_console.cpython-310.pyc
    │           │   │   │   │   ├── _windows.cpython-310.pyc
    │           │   │   │   │   ├── _windows_renderer.cpython-310.pyc
    │           │   │   │   │   ├── _wrap.cpython-310.pyc
    │           │   │   │   │   ├── abc.cpython-310.pyc
    │           │   │   │   │   ├── align.cpython-310.pyc
    │           │   │   │   │   ├── ansi.cpython-310.pyc
    │           │   │   │   │   ├── bar.cpython-310.pyc
    │           │   │   │   │   ├── box.cpython-310.pyc
    │           │   │   │   │   ├── cells.cpython-310.pyc
    │           │   │   │   │   ├── color.cpython-310.pyc
    │           │   │   │   │   ├── color_triplet.cpython-310.pyc
    │           │   │   │   │   ├── columns.cpython-310.pyc
    │           │   │   │   │   ├── console.cpython-310.pyc
    │           │   │   │   │   ├── constrain.cpython-310.pyc
    │           │   │   │   │   ├── containers.cpython-310.pyc
    │           │   │   │   │   ├── control.cpython-310.pyc
    │           │   │   │   │   ├── default_styles.cpython-310.pyc
    │           │   │   │   │   ├── diagnose.cpython-310.pyc
    │           │   │   │   │   ├── emoji.cpython-310.pyc
    │           │   │   │   │   ├── errors.cpython-310.pyc
    │           │   │   │   │   ├── file_proxy.cpython-310.pyc
    │           │   │   │   │   ├── filesize.cpython-310.pyc
    │           │   │   │   │   ├── highlighter.cpython-310.pyc
    │           │   │   │   │   ├── json.cpython-310.pyc
    │           │   │   │   │   ├── jupyter.cpython-310.pyc
    │           │   │   │   │   ├── layout.cpython-310.pyc
    │           │   │   │   │   ├── live.cpython-310.pyc
    │           │   │   │   │   ├── live_render.cpython-310.pyc
    │           │   │   │   │   ├── logging.cpython-310.pyc
    │           │   │   │   │   ├── markup.cpython-310.pyc
    │           │   │   │   │   ├── measure.cpython-310.pyc
    │           │   │   │   │   ├── padding.cpython-310.pyc
    │           │   │   │   │   ├── pager.cpython-310.pyc
    │           │   │   │   │   ├── palette.cpython-310.pyc
    │           │   │   │   │   ├── panel.cpython-310.pyc
    │           │   │   │   │   ├── pretty.cpython-310.pyc
    │           │   │   │   │   ├── progress.cpython-310.pyc
    │           │   │   │   │   ├── progress_bar.cpython-310.pyc
    │           │   │   │   │   ├── prompt.cpython-310.pyc
    │           │   │   │   │   ├── protocol.cpython-310.pyc
    │           │   │   │   │   ├── region.cpython-310.pyc
    │           │   │   │   │   ├── repr.cpython-310.pyc
    │           │   │   │   │   ├── rule.cpython-310.pyc
    │           │   │   │   │   ├── scope.cpython-310.pyc
    │           │   │   │   │   ├── screen.cpython-310.pyc
    │           │   │   │   │   ├── segment.cpython-310.pyc
    │           │   │   │   │   ├── spinner.cpython-310.pyc
    │           │   │   │   │   ├── status.cpython-310.pyc
    │           │   │   │   │   ├── style.cpython-310.pyc
    │           │   │   │   │   ├── styled.cpython-310.pyc
    │           │   │   │   │   ├── syntax.cpython-310.pyc
    │           │   │   │   │   ├── table.cpython-310.pyc
    │           │   │   │   │   ├── terminal_theme.cpython-310.pyc
    │           │   │   │   │   ├── text.cpython-310.pyc
    │           │   │   │   │   ├── theme.cpython-310.pyc
    │           │   │   │   │   ├── themes.cpython-310.pyc
    │           │   │   │   │   ├── traceback.cpython-310.pyc
    │           │   │   │   │   └── tree.cpython-310.pyc
    │           │   │   │   ├── _cell_widths.py
    │           │   │   │   ├── _emoji_codes.py
    │           │   │   │   ├── _emoji_replace.py
    │           │   │   │   ├── _export_format.py
    │           │   │   │   ├── _extension.py
    │           │   │   │   ├── _fileno.py
    │           │   │   │   ├── _inspect.py
    │           │   │   │   ├── _log_render.py
    │           │   │   │   ├── _loop.py
    │           │   │   │   ├── _null_file.py
    │           │   │   │   ├── _palettes.py
    │           │   │   │   ├── _pick.py
    │           │   │   │   ├── _ratio.py
    │           │   │   │   ├── _spinners.py
    │           │   │   │   ├── _stack.py
    │           │   │   │   ├── _timer.py
    │           │   │   │   ├── _win32_console.py
    │           │   │   │   ├── _windows.py
    │           │   │   │   ├── _windows_renderer.py
    │           │   │   │   ├── _wrap.py
    │           │   │   │   ├── abc.py
    │           │   │   │   ├── align.py
    │           │   │   │   ├── ansi.py
    │           │   │   │   ├── bar.py
    │           │   │   │   ├── box.py
    │           │   │   │   ├── cells.py
    │           │   │   │   ├── color.py
    │           │   │   │   ├── color_triplet.py
    │           │   │   │   ├── columns.py
    │           │   │   │   ├── console.py
    │           │   │   │   ├── constrain.py
    │           │   │   │   ├── containers.py
    │           │   │   │   ├── control.py
    │           │   │   │   ├── default_styles.py
    │           │   │   │   ├── diagnose.py
    │           │   │   │   ├── emoji.py
    │           │   │   │   ├── errors.py
    │           │   │   │   ├── file_proxy.py
    │           │   │   │   ├── filesize.py
    │           │   │   │   ├── highlighter.py
    │           │   │   │   ├── json.py
    │           │   │   │   ├── jupyter.py
    │           │   │   │   ├── layout.py
    │           │   │   │   ├── live.py
    │           │   │   │   ├── live_render.py
    │           │   │   │   ├── logging.py
    │           │   │   │   ├── markup.py
    │           │   │   │   ├── measure.py
    │           │   │   │   ├── padding.py
    │           │   │   │   ├── pager.py
    │           │   │   │   ├── palette.py
    │           │   │   │   ├── panel.py
    │           │   │   │   ├── pretty.py
    │           │   │   │   ├── progress.py
    │           │   │   │   ├── progress_bar.py
    │           │   │   │   ├── prompt.py
    │           │   │   │   ├── protocol.py
    │           │   │   │   ├── py.typed
    │           │   │   │   ├── region.py
    │           │   │   │   ├── repr.py
    │           │   │   │   ├── rule.py
    │           │   │   │   ├── scope.py
    │           │   │   │   ├── screen.py
    │           │   │   │   ├── segment.py
    │           │   │   │   ├── spinner.py
    │           │   │   │   ├── status.py
    │           │   │   │   ├── style.py
    │           │   │   │   ├── styled.py
    │           │   │   │   ├── syntax.py
    │           │   │   │   ├── table.py
    │           │   │   │   ├── terminal_theme.py
    │           │   │   │   ├── text.py
    │           │   │   │   ├── theme.py
    │           │   │   │   ├── themes.py
    │           │   │   │   ├── traceback.py
    │           │   │   │   └── tree.py
    │           │   │   ├── tomli
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── _parser.cpython-310.pyc
    │           │   │   │   │   ├── _re.cpython-310.pyc
    │           │   │   │   │   └── _types.cpython-310.pyc
    │           │   │   │   ├── _parser.py
    │           │   │   │   ├── _re.py
    │           │   │   │   ├── _types.py
    │           │   │   │   └── py.typed
    │           │   │   ├── tomli_w
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   └── _writer.cpython-310.pyc
    │           │   │   │   ├── _writer.py
    │           │   │   │   └── py.typed
    │           │   │   ├── truststore
    │           │   │   │   ├── LICENSE
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── _api.cpython-310.pyc
    │           │   │   │   │   ├── _macos.cpython-310.pyc
    │           │   │   │   │   ├── _openssl.cpython-310.pyc
    │           │   │   │   │   ├── _ssl_constants.cpython-310.pyc
    │           │   │   │   │   └── _windows.cpython-310.pyc
    │           │   │   │   ├── _api.py
    │           │   │   │   ├── _macos.py
    │           │   │   │   ├── _openssl.py
    │           │   │   │   ├── _ssl_constants.py
    │           │   │   │   ├── _windows.py
    │           │   │   │   └── py.typed
    │           │   │   ├── urllib3
    │           │   │   │   ├── LICENSE.txt
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── _collections.cpython-310.pyc
    │           │   │   │   │   ├── _version.cpython-310.pyc
    │           │   │   │   │   ├── connection.cpython-310.pyc
    │           │   │   │   │   ├── connectionpool.cpython-310.pyc
    │           │   │   │   │   ├── exceptions.cpython-310.pyc
    │           │   │   │   │   ├── fields.cpython-310.pyc
    │           │   │   │   │   ├── filepost.cpython-310.pyc
    │           │   │   │   │   ├── poolmanager.cpython-310.pyc
    │           │   │   │   │   ├── request.cpython-310.pyc
    │           │   │   │   │   └── response.cpython-310.pyc
    │           │   │   │   ├── _collections.py
    │           │   │   │   ├── _version.py
    │           │   │   │   ├── connection.py
    │           │   │   │   ├── connectionpool.py
    │           │   │   │   ├── contrib
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   ├── _appengine_environ.cpython-310.pyc
    │           │   │   │   │   │   ├── appengine.cpython-310.pyc
    │           │   │   │   │   │   ├── ntlmpool.cpython-310.pyc
    │           │   │   │   │   │   ├── pyopenssl.cpython-310.pyc
    │           │   │   │   │   │   ├── securetransport.cpython-310.pyc
    │           │   │   │   │   │   └── socks.cpython-310.pyc
    │           │   │   │   │   ├── _appengine_environ.py
    │           │   │   │   │   ├── _securetransport
    │           │   │   │   │   │   ├── __init__.py
    │           │   │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   │   ├── bindings.cpython-310.pyc
    │           │   │   │   │   │   │   └── low_level.cpython-310.pyc
    │           │   │   │   │   │   ├── bindings.py
    │           │   │   │   │   │   └── low_level.py
    │           │   │   │   │   ├── appengine.py
    │           │   │   │   │   ├── ntlmpool.py
    │           │   │   │   │   ├── pyopenssl.py
    │           │   │   │   │   ├── securetransport.py
    │           │   │   │   │   └── socks.py
    │           │   │   │   ├── exceptions.py
    │           │   │   │   ├── fields.py
    │           │   │   │   ├── filepost.py
    │           │   │   │   ├── packages
    │           │   │   │   │   ├── __init__.py
    │           │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   └── six.cpython-310.pyc
    │           │   │   │   │   ├── backports
    │           │   │   │   │   │   ├── __init__.py
    │           │   │   │   │   │   ├── __pycache__
    │           │   │   │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   │   │   ├── makefile.cpython-310.pyc
    │           │   │   │   │   │   │   └── weakref_finalize.cpython-310.pyc
    │           │   │   │   │   │   ├── makefile.py
    │           │   │   │   │   │   └── weakref_finalize.py
    │           │   │   │   │   └── six.py
    │           │   │   │   ├── poolmanager.py
    │           │   │   │   ├── request.py
    │           │   │   │   ├── response.py
    │           │   │   │   └── util
    │           │   │   │       ├── __init__.py
    │           │   │   │       ├── __pycache__
    │           │   │   │       │   ├── __init__.cpython-310.pyc
    │           │   │   │       │   ├── connection.cpython-310.pyc
    │           │   │   │       │   ├── proxy.cpython-310.pyc
    │           │   │   │       │   ├── queue.cpython-310.pyc
    │           │   │   │       │   ├── request.cpython-310.pyc
    │           │   │   │       │   ├── response.cpython-310.pyc
    │           │   │   │       │   ├── retry.cpython-310.pyc
    │           │   │   │       │   ├── ssl_.cpython-310.pyc
    │           │   │   │       │   ├── ssl_match_hostname.cpython-310.pyc
    │           │   │   │       │   ├── ssltransport.cpython-310.pyc
    │           │   │   │       │   ├── timeout.cpython-310.pyc
    │           │   │   │       │   ├── url.cpython-310.pyc
    │           │   │   │       │   └── wait.cpython-310.pyc
    │           │   │   │       ├── connection.py
    │           │   │   │       ├── proxy.py
    │           │   │   │       ├── queue.py
    │           │   │   │       ├── request.py
    │           │   │   │       ├── response.py
    │           │   │   │       ├── retry.py
    │           │   │   │       ├── ssl_.py
    │           │   │   │       ├── ssl_match_hostname.py
    │           │   │   │       ├── ssltransport.py
    │           │   │   │       ├── timeout.py
    │           │   │   │       ├── url.py
    │           │   │   │       └── wait.py
    │           │   │   └── vendor.txt
    │           │   └── py.typed
    │           ├── pip-26.0.1.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── REQUESTED
    │           │   ├── WHEEL
    │           │   ├── entry_points.txt
    │           │   └── licenses
    │           │       ├── AUTHORS.txt
    │           │       ├── LICENSE.txt
    │           │       └── src
    │           │           └── pip
    │           │               └── _vendor
    │           │                   ├── cachecontrol
    │           │                   │   └── LICENSE.txt
    │           │                   ├── certifi
    │           │                   │   └── LICENSE
    │           │                   ├── dependency_groups
    │           │                   │   └── LICENSE.txt
    │           │                   ├── distlib
    │           │                   │   └── LICENSE.txt
    │           │                   ├── distro
    │           │                   │   └── LICENSE
    │           │                   ├── idna
    │           │                   │   └── LICENSE.md
    │           │                   ├── msgpack
    │           │                   │   └── COPYING
    │           │                   ├── packaging
    │           │                   │   ├── LICENSE
    │           │                   │   ├── LICENSE.APACHE
    │           │                   │   └── LICENSE.BSD
    │           │                   ├── pkg_resources
    │           │                   │   └── LICENSE
    │           │                   ├── platformdirs
    │           │                   │   └── LICENSE
    │           │                   ├── pygments
    │           │                   │   └── LICENSE
    │           │                   ├── pyproject_hooks
    │           │                   │   └── LICENSE
    │           │                   ├── requests
    │           │                   │   └── LICENSE
    │           │                   ├── resolvelib
    │           │                   │   └── LICENSE
    │           │                   ├── rich
    │           │                   │   └── LICENSE
    │           │                   ├── tomli
    │           │                   │   └── LICENSE
    │           │                   ├── tomli_w
    │           │                   │   └── LICENSE
    │           │                   ├── truststore
    │           │                   │   └── LICENSE
    │           │                   └── urllib3
    │           │                       └── LICENSE.txt
    │           ├── pkg_resources
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   └── __init__.cpython-310.pyc
    │           │   ├── _vendor
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── appdirs.cpython-310.pyc
    │           │   │   │   └── pyparsing.cpython-310.pyc
    │           │   │   ├── appdirs.py
    │           │   │   ├── packaging
    │           │   │   │   ├── __about__.py
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __about__.cpython-310.pyc
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── _manylinux.cpython-310.pyc
    │           │   │   │   │   ├── _musllinux.cpython-310.pyc
    │           │   │   │   │   ├── _structures.cpython-310.pyc
    │           │   │   │   │   ├── markers.cpython-310.pyc
    │           │   │   │   │   ├── requirements.cpython-310.pyc
    │           │   │   │   │   ├── specifiers.cpython-310.pyc
    │           │   │   │   │   ├── tags.cpython-310.pyc
    │           │   │   │   │   ├── utils.cpython-310.pyc
    │           │   │   │   │   └── version.cpython-310.pyc
    │           │   │   │   ├── _manylinux.py
    │           │   │   │   ├── _musllinux.py
    │           │   │   │   ├── _structures.py
    │           │   │   │   ├── markers.py
    │           │   │   │   ├── requirements.py
    │           │   │   │   ├── specifiers.py
    │           │   │   │   ├── tags.py
    │           │   │   │   ├── utils.py
    │           │   │   │   └── version.py
    │           │   │   └── pyparsing.py
    │           │   ├── extern
    │           │   │   ├── __init__.py
    │           │   │   └── __pycache__
    │           │   │       └── __init__.cpython-310.pyc
    │           │   └── tests
    │           │       └── data
    │           │           └── my-test-package-source
    │           │               ├── __pycache__
    │           │               │   └── setup.cpython-310.pyc
    │           │               └── setup.py
    │           ├── pygments
    │           │   ├── __init__.py
    │           │   ├── __main__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── __main__.cpython-310.pyc
    │           │   │   ├── cmdline.cpython-310.pyc
    │           │   │   ├── console.cpython-310.pyc
    │           │   │   ├── filter.cpython-310.pyc
    │           │   │   ├── formatter.cpython-310.pyc
    │           │   │   ├── lexer.cpython-310.pyc
    │           │   │   ├── modeline.cpython-310.pyc
    │           │   │   ├── plugin.cpython-310.pyc
    │           │   │   ├── regexopt.cpython-310.pyc
    │           │   │   ├── scanner.cpython-310.pyc
    │           │   │   ├── sphinxext.cpython-310.pyc
    │           │   │   ├── style.cpython-310.pyc
    │           │   │   ├── token.cpython-310.pyc
    │           │   │   ├── unistring.cpython-310.pyc
    │           │   │   └── util.cpython-310.pyc
    │           │   ├── cmdline.py
    │           │   ├── console.py
    │           │   ├── filter.py
    │           │   ├── filters
    │           │   │   ├── __init__.py
    │           │   │   └── __pycache__
    │           │   │       └── __init__.cpython-310.pyc
    │           │   ├── formatter.py
    │           │   ├── formatters
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── _mapping.cpython-310.pyc
    │           │   │   │   ├── bbcode.cpython-310.pyc
    │           │   │   │   ├── groff.cpython-310.pyc
    │           │   │   │   ├── html.cpython-310.pyc
    │           │   │   │   ├── img.cpython-310.pyc
    │           │   │   │   ├── irc.cpython-310.pyc
    │           │   │   │   ├── latex.cpython-310.pyc
    │           │   │   │   ├── other.cpython-310.pyc
    │           │   │   │   ├── pangomarkup.cpython-310.pyc
    │           │   │   │   ├── rtf.cpython-310.pyc
    │           │   │   │   ├── svg.cpython-310.pyc
    │           │   │   │   ├── terminal.cpython-310.pyc
    │           │   │   │   └── terminal256.cpython-310.pyc
    │           │   │   ├── _mapping.py
    │           │   │   ├── bbcode.py
    │           │   │   ├── groff.py
    │           │   │   ├── html.py
    │           │   │   ├── img.py
    │           │   │   ├── irc.py
    │           │   │   ├── latex.py
    │           │   │   ├── other.py
    │           │   │   ├── pangomarkup.py
    │           │   │   ├── rtf.py
    │           │   │   ├── svg.py
    │           │   │   ├── terminal.py
    │           │   │   └── terminal256.py
    │           │   ├── lexer.py
    │           │   ├── lexers
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── _ada_builtins.cpython-310.pyc
    │           │   │   │   ├── _asy_builtins.cpython-310.pyc
    │           │   │   │   ├── _cl_builtins.cpython-310.pyc
    │           │   │   │   ├── _cocoa_builtins.cpython-310.pyc
    │           │   │   │   ├── _csound_builtins.cpython-310.pyc
    │           │   │   │   ├── _css_builtins.cpython-310.pyc
    │           │   │   │   ├── _googlesql_builtins.cpython-310.pyc
    │           │   │   │   ├── _julia_builtins.cpython-310.pyc
    │           │   │   │   ├── _lasso_builtins.cpython-310.pyc
    │           │   │   │   ├── _lilypond_builtins.cpython-310.pyc
    │           │   │   │   ├── _lua_builtins.cpython-310.pyc
    │           │   │   │   ├── _luau_builtins.cpython-310.pyc
    │           │   │   │   ├── _mapping.cpython-310.pyc
    │           │   │   │   ├── _mql_builtins.cpython-310.pyc
    │           │   │   │   ├── _mysql_builtins.cpython-310.pyc
    │           │   │   │   ├── _openedge_builtins.cpython-310.pyc
    │           │   │   │   ├── _php_builtins.cpython-310.pyc
    │           │   │   │   ├── _postgres_builtins.cpython-310.pyc
    │           │   │   │   ├── _qlik_builtins.cpython-310.pyc
    │           │   │   │   ├── _scheme_builtins.cpython-310.pyc
    │           │   │   │   ├── _scilab_builtins.cpython-310.pyc
    │           │   │   │   ├── _sourcemod_builtins.cpython-310.pyc
    │           │   │   │   ├── _sql_builtins.cpython-310.pyc
    │           │   │   │   ├── _stan_builtins.cpython-310.pyc
    │           │   │   │   ├── _stata_builtins.cpython-310.pyc
    │           │   │   │   ├── _tsql_builtins.cpython-310.pyc
    │           │   │   │   ├── _usd_builtins.cpython-310.pyc
    │           │   │   │   ├── _vbscript_builtins.cpython-310.pyc
    │           │   │   │   ├── _vim_builtins.cpython-310.pyc
    │           │   │   │   ├── actionscript.cpython-310.pyc
    │           │   │   │   ├── ada.cpython-310.pyc
    │           │   │   │   ├── agile.cpython-310.pyc
    │           │   │   │   ├── algebra.cpython-310.pyc
    │           │   │   │   ├── ambient.cpython-310.pyc
    │           │   │   │   ├── amdgpu.cpython-310.pyc
    │           │   │   │   ├── ampl.cpython-310.pyc
    │           │   │   │   ├── apdlexer.cpython-310.pyc
    │           │   │   │   ├── apl.cpython-310.pyc
    │           │   │   │   ├── archetype.cpython-310.pyc
    │           │   │   │   ├── arrow.cpython-310.pyc
    │           │   │   │   ├── arturo.cpython-310.pyc
    │           │   │   │   ├── asc.cpython-310.pyc
    │           │   │   │   ├── asm.cpython-310.pyc
    │           │   │   │   ├── asn1.cpython-310.pyc
    │           │   │   │   ├── automation.cpython-310.pyc
    │           │   │   │   ├── bare.cpython-310.pyc
    │           │   │   │   ├── basic.cpython-310.pyc
    │           │   │   │   ├── bdd.cpython-310.pyc
    │           │   │   │   ├── berry.cpython-310.pyc
    │           │   │   │   ├── bibtex.cpython-310.pyc
    │           │   │   │   ├── blueprint.cpython-310.pyc
    │           │   │   │   ├── boa.cpython-310.pyc
    │           │   │   │   ├── bqn.cpython-310.pyc
    │           │   │   │   ├── business.cpython-310.pyc
    │           │   │   │   ├── c_cpp.cpython-310.pyc
    │           │   │   │   ├── c_like.cpython-310.pyc
    │           │   │   │   ├── capnproto.cpython-310.pyc
    │           │   │   │   ├── carbon.cpython-310.pyc
    │           │   │   │   ├── cddl.cpython-310.pyc
    │           │   │   │   ├── chapel.cpython-310.pyc
    │           │   │   │   ├── clean.cpython-310.pyc
    │           │   │   │   ├── codeql.cpython-310.pyc
    │           │   │   │   ├── comal.cpython-310.pyc
    │           │   │   │   ├── compiled.cpython-310.pyc
    │           │   │   │   ├── configs.cpython-310.pyc
    │           │   │   │   ├── console.cpython-310.pyc
    │           │   │   │   ├── cplint.cpython-310.pyc
    │           │   │   │   ├── crystal.cpython-310.pyc
    │           │   │   │   ├── csound.cpython-310.pyc
    │           │   │   │   ├── css.cpython-310.pyc
    │           │   │   │   ├── d.cpython-310.pyc
    │           │   │   │   ├── dalvik.cpython-310.pyc
    │           │   │   │   ├── data.cpython-310.pyc
    │           │   │   │   ├── dax.cpython-310.pyc
    │           │   │   │   ├── devicetree.cpython-310.pyc
    │           │   │   │   ├── diff.cpython-310.pyc
    │           │   │   │   ├── dns.cpython-310.pyc
    │           │   │   │   ├── dotnet.cpython-310.pyc
    │           │   │   │   ├── dsls.cpython-310.pyc
    │           │   │   │   ├── dylan.cpython-310.pyc
    │           │   │   │   ├── ecl.cpython-310.pyc
    │           │   │   │   ├── eiffel.cpython-310.pyc
    │           │   │   │   ├── elm.cpython-310.pyc
    │           │   │   │   ├── elpi.cpython-310.pyc
    │           │   │   │   ├── email.cpython-310.pyc
    │           │   │   │   ├── erlang.cpython-310.pyc
    │           │   │   │   ├── esoteric.cpython-310.pyc
    │           │   │   │   ├── ezhil.cpython-310.pyc
    │           │   │   │   ├── factor.cpython-310.pyc
    │           │   │   │   ├── fantom.cpython-310.pyc
    │           │   │   │   ├── felix.cpython-310.pyc
    │           │   │   │   ├── fift.cpython-310.pyc
    │           │   │   │   ├── floscript.cpython-310.pyc
    │           │   │   │   ├── forth.cpython-310.pyc
    │           │   │   │   ├── fortran.cpython-310.pyc
    │           │   │   │   ├── foxpro.cpython-310.pyc
    │           │   │   │   ├── freefem.cpython-310.pyc
    │           │   │   │   ├── func.cpython-310.pyc
    │           │   │   │   ├── functional.cpython-310.pyc
    │           │   │   │   ├── futhark.cpython-310.pyc
    │           │   │   │   ├── gcodelexer.cpython-310.pyc
    │           │   │   │   ├── gdscript.cpython-310.pyc
    │           │   │   │   ├── gleam.cpython-310.pyc
    │           │   │   │   ├── go.cpython-310.pyc
    │           │   │   │   ├── grammar_notation.cpython-310.pyc
    │           │   │   │   ├── graph.cpython-310.pyc
    │           │   │   │   ├── graphics.cpython-310.pyc
    │           │   │   │   ├── graphql.cpython-310.pyc
    │           │   │   │   ├── graphviz.cpython-310.pyc
    │           │   │   │   ├── gsql.cpython-310.pyc
    │           │   │   │   ├── hare.cpython-310.pyc
    │           │   │   │   ├── haskell.cpython-310.pyc
    │           │   │   │   ├── haxe.cpython-310.pyc
    │           │   │   │   ├── hdl.cpython-310.pyc
    │           │   │   │   ├── hexdump.cpython-310.pyc
    │           │   │   │   ├── html.cpython-310.pyc
    │           │   │   │   ├── idl.cpython-310.pyc
    │           │   │   │   ├── igor.cpython-310.pyc
    │           │   │   │   ├── inferno.cpython-310.pyc
    │           │   │   │   ├── installers.cpython-310.pyc
    │           │   │   │   ├── int_fiction.cpython-310.pyc
    │           │   │   │   ├── iolang.cpython-310.pyc
    │           │   │   │   ├── j.cpython-310.pyc
    │           │   │   │   ├── javascript.cpython-310.pyc
    │           │   │   │   ├── jmespath.cpython-310.pyc
    │           │   │   │   ├── jslt.cpython-310.pyc
    │           │   │   │   ├── json5.cpython-310.pyc
    │           │   │   │   ├── jsonnet.cpython-310.pyc
    │           │   │   │   ├── jsx.cpython-310.pyc
    │           │   │   │   ├── julia.cpython-310.pyc
    │           │   │   │   ├── jvm.cpython-310.pyc
    │           │   │   │   ├── kuin.cpython-310.pyc
    │           │   │   │   ├── kusto.cpython-310.pyc
    │           │   │   │   ├── ldap.cpython-310.pyc
    │           │   │   │   ├── lean.cpython-310.pyc
    │           │   │   │   ├── lilypond.cpython-310.pyc
    │           │   │   │   ├── lisp.cpython-310.pyc
    │           │   │   │   ├── macaulay2.cpython-310.pyc
    │           │   │   │   ├── make.cpython-310.pyc
    │           │   │   │   ├── maple.cpython-310.pyc
    │           │   │   │   ├── markup.cpython-310.pyc
    │           │   │   │   ├── math.cpython-310.pyc
    │           │   │   │   ├── matlab.cpython-310.pyc
    │           │   │   │   ├── maxima.cpython-310.pyc
    │           │   │   │   ├── meson.cpython-310.pyc
    │           │   │   │   ├── mime.cpython-310.pyc
    │           │   │   │   ├── minecraft.cpython-310.pyc
    │           │   │   │   ├── mips.cpython-310.pyc
    │           │   │   │   ├── ml.cpython-310.pyc
    │           │   │   │   ├── modeling.cpython-310.pyc
    │           │   │   │   ├── modula2.cpython-310.pyc
    │           │   │   │   ├── mojo.cpython-310.pyc
    │           │   │   │   ├── monte.cpython-310.pyc
    │           │   │   │   ├── mosel.cpython-310.pyc
    │           │   │   │   ├── ncl.cpython-310.pyc
    │           │   │   │   ├── nimrod.cpython-310.pyc
    │           │   │   │   ├── nit.cpython-310.pyc
    │           │   │   │   ├── nix.cpython-310.pyc
    │           │   │   │   ├── numbair.cpython-310.pyc
    │           │   │   │   ├── oberon.cpython-310.pyc
    │           │   │   │   ├── objective.cpython-310.pyc
    │           │   │   │   ├── ooc.cpython-310.pyc
    │           │   │   │   ├── openscad.cpython-310.pyc
    │           │   │   │   ├── other.cpython-310.pyc
    │           │   │   │   ├── parasail.cpython-310.pyc
    │           │   │   │   ├── parsers.cpython-310.pyc
    │           │   │   │   ├── pascal.cpython-310.pyc
    │           │   │   │   ├── pawn.cpython-310.pyc
    │           │   │   │   ├── pddl.cpython-310.pyc
    │           │   │   │   ├── perl.cpython-310.pyc
    │           │   │   │   ├── phix.cpython-310.pyc
    │           │   │   │   ├── php.cpython-310.pyc
    │           │   │   │   ├── pointless.cpython-310.pyc
    │           │   │   │   ├── pony.cpython-310.pyc
    │           │   │   │   ├── praat.cpython-310.pyc
    │           │   │   │   ├── procfile.cpython-310.pyc
    │           │   │   │   ├── prolog.cpython-310.pyc
    │           │   │   │   ├── promql.cpython-310.pyc
    │           │   │   │   ├── prql.cpython-310.pyc
    │           │   │   │   ├── ptx.cpython-310.pyc
    │           │   │   │   ├── python.cpython-310.pyc
    │           │   │   │   ├── q.cpython-310.pyc
    │           │   │   │   ├── qlik.cpython-310.pyc
    │           │   │   │   ├── qvt.cpython-310.pyc
    │           │   │   │   ├── r.cpython-310.pyc
    │           │   │   │   ├── rdf.cpython-310.pyc
    │           │   │   │   ├── rebol.cpython-310.pyc
    │           │   │   │   ├── rego.cpython-310.pyc
    │           │   │   │   ├── resource.cpython-310.pyc
    │           │   │   │   ├── ride.cpython-310.pyc
    │           │   │   │   ├── rita.cpython-310.pyc
    │           │   │   │   ├── rnc.cpython-310.pyc
    │           │   │   │   ├── roboconf.cpython-310.pyc
    │           │   │   │   ├── robotframework.cpython-310.pyc
    │           │   │   │   ├── ruby.cpython-310.pyc
    │           │   │   │   ├── rust.cpython-310.pyc
    │           │   │   │   ├── sas.cpython-310.pyc
    │           │   │   │   ├── savi.cpython-310.pyc
    │           │   │   │   ├── scdoc.cpython-310.pyc
    │           │   │   │   ├── scripting.cpython-310.pyc
    │           │   │   │   ├── sgf.cpython-310.pyc
    │           │   │   │   ├── shell.cpython-310.pyc
    │           │   │   │   ├── sieve.cpython-310.pyc
    │           │   │   │   ├── slash.cpython-310.pyc
    │           │   │   │   ├── smalltalk.cpython-310.pyc
    │           │   │   │   ├── smithy.cpython-310.pyc
    │           │   │   │   ├── smv.cpython-310.pyc
    │           │   │   │   ├── snobol.cpython-310.pyc
    │           │   │   │   ├── solidity.cpython-310.pyc
    │           │   │   │   ├── soong.cpython-310.pyc
    │           │   │   │   ├── sophia.cpython-310.pyc
    │           │   │   │   ├── special.cpython-310.pyc
    │           │   │   │   ├── spice.cpython-310.pyc
    │           │   │   │   ├── sql.cpython-310.pyc
    │           │   │   │   ├── srcinfo.cpython-310.pyc
    │           │   │   │   ├── stata.cpython-310.pyc
    │           │   │   │   ├── supercollider.cpython-310.pyc
    │           │   │   │   ├── tablegen.cpython-310.pyc
    │           │   │   │   ├── tact.cpython-310.pyc
    │           │   │   │   ├── tal.cpython-310.pyc
    │           │   │   │   ├── tcl.cpython-310.pyc
    │           │   │   │   ├── teal.cpython-310.pyc
    │           │   │   │   ├── templates.cpython-310.pyc
    │           │   │   │   ├── teraterm.cpython-310.pyc
    │           │   │   │   ├── testing.cpython-310.pyc
    │           │   │   │   ├── text.cpython-310.pyc
    │           │   │   │   ├── textedit.cpython-310.pyc
    │           │   │   │   ├── textfmts.cpython-310.pyc
    │           │   │   │   ├── theorem.cpython-310.pyc
    │           │   │   │   ├── thingsdb.cpython-310.pyc
    │           │   │   │   ├── tlb.cpython-310.pyc
    │           │   │   │   ├── tls.cpython-310.pyc
    │           │   │   │   ├── tnt.cpython-310.pyc
    │           │   │   │   ├── trafficscript.cpython-310.pyc
    │           │   │   │   ├── typoscript.cpython-310.pyc
    │           │   │   │   ├── typst.cpython-310.pyc
    │           │   │   │   ├── ul4.cpython-310.pyc
    │           │   │   │   ├── unicon.cpython-310.pyc
    │           │   │   │   ├── urbi.cpython-310.pyc
    │           │   │   │   ├── usd.cpython-310.pyc
    │           │   │   │   ├── varnish.cpython-310.pyc
    │           │   │   │   ├── verification.cpython-310.pyc
    │           │   │   │   ├── verifpal.cpython-310.pyc
    │           │   │   │   ├── vip.cpython-310.pyc
    │           │   │   │   ├── vyper.cpython-310.pyc
    │           │   │   │   ├── web.cpython-310.pyc
    │           │   │   │   ├── webassembly.cpython-310.pyc
    │           │   │   │   ├── webidl.cpython-310.pyc
    │           │   │   │   ├── webmisc.cpython-310.pyc
    │           │   │   │   ├── wgsl.cpython-310.pyc
    │           │   │   │   ├── whiley.cpython-310.pyc
    │           │   │   │   ├── wowtoc.cpython-310.pyc
    │           │   │   │   ├── wren.cpython-310.pyc
    │           │   │   │   ├── x10.cpython-310.pyc
    │           │   │   │   ├── xorg.cpython-310.pyc
    │           │   │   │   ├── yang.cpython-310.pyc
    │           │   │   │   ├── yara.cpython-310.pyc
    │           │   │   │   └── zig.cpython-310.pyc
    │           │   │   ├── _ada_builtins.py
    │           │   │   ├── _asy_builtins.py
    │           │   │   ├── _cl_builtins.py
    │           │   │   ├── _cocoa_builtins.py
    │           │   │   ├── _csound_builtins.py
    │           │   │   ├── _css_builtins.py
    │           │   │   ├── _googlesql_builtins.py
    │           │   │   ├── _julia_builtins.py
    │           │   │   ├── _lasso_builtins.py
    │           │   │   ├── _lilypond_builtins.py
    │           │   │   ├── _lua_builtins.py
    │           │   │   ├── _luau_builtins.py
    │           │   │   ├── _mapping.py
    │           │   │   ├── _mql_builtins.py
    │           │   │   ├── _mysql_builtins.py
    │           │   │   ├── _openedge_builtins.py
    │           │   │   ├── _php_builtins.py
    │           │   │   ├── _postgres_builtins.py
    │           │   │   ├── _qlik_builtins.py
    │           │   │   ├── _scheme_builtins.py
    │           │   │   ├── _scilab_builtins.py
    │           │   │   ├── _sourcemod_builtins.py
    │           │   │   ├── _sql_builtins.py
    │           │   │   ├── _stan_builtins.py
    │           │   │   ├── _stata_builtins.py
    │           │   │   ├── _tsql_builtins.py
    │           │   │   ├── _usd_builtins.py
    │           │   │   ├── _vbscript_builtins.py
    │           │   │   ├── _vim_builtins.py
    │           │   │   ├── actionscript.py
    │           │   │   ├── ada.py
    │           │   │   ├── agile.py
    │           │   │   ├── algebra.py
    │           │   │   ├── ambient.py
    │           │   │   ├── amdgpu.py
    │           │   │   ├── ampl.py
    │           │   │   ├── apdlexer.py
    │           │   │   ├── apl.py
    │           │   │   ├── archetype.py
    │           │   │   ├── arrow.py
    │           │   │   ├── arturo.py
    │           │   │   ├── asc.py
    │           │   │   ├── asm.py
    │           │   │   ├── asn1.py
    │           │   │   ├── automation.py
    │           │   │   ├── bare.py
    │           │   │   ├── basic.py
    │           │   │   ├── bdd.py
    │           │   │   ├── berry.py
    │           │   │   ├── bibtex.py
    │           │   │   ├── blueprint.py
    │           │   │   ├── boa.py
    │           │   │   ├── bqn.py
    │           │   │   ├── business.py
    │           │   │   ├── c_cpp.py
    │           │   │   ├── c_like.py
    │           │   │   ├── capnproto.py
    │           │   │   ├── carbon.py
    │           │   │   ├── cddl.py
    │           │   │   ├── chapel.py
    │           │   │   ├── clean.py
    │           │   │   ├── codeql.py
    │           │   │   ├── comal.py
    │           │   │   ├── compiled.py
    │           │   │   ├── configs.py
    │           │   │   ├── console.py
    │           │   │   ├── cplint.py
    │           │   │   ├── crystal.py
    │           │   │   ├── csound.py
    │           │   │   ├── css.py
    │           │   │   ├── d.py
    │           │   │   ├── dalvik.py
    │           │   │   ├── data.py
    │           │   │   ├── dax.py
    │           │   │   ├── devicetree.py
    │           │   │   ├── diff.py
    │           │   │   ├── dns.py
    │           │   │   ├── dotnet.py
    │           │   │   ├── dsls.py
    │           │   │   ├── dylan.py
    │           │   │   ├── ecl.py
    │           │   │   ├── eiffel.py
    │           │   │   ├── elm.py
    │           │   │   ├── elpi.py
    │           │   │   ├── email.py
    │           │   │   ├── erlang.py
    │           │   │   ├── esoteric.py
    │           │   │   ├── ezhil.py
    │           │   │   ├── factor.py
    │           │   │   ├── fantom.py
    │           │   │   ├── felix.py
    │           │   │   ├── fift.py
    │           │   │   ├── floscript.py
    │           │   │   ├── forth.py
    │           │   │   ├── fortran.py
    │           │   │   ├── foxpro.py
    │           │   │   ├── freefem.py
    │           │   │   ├── func.py
    │           │   │   ├── functional.py
    │           │   │   ├── futhark.py
    │           │   │   ├── gcodelexer.py
    │           │   │   ├── gdscript.py
    │           │   │   ├── gleam.py
    │           │   │   ├── go.py
    │           │   │   ├── grammar_notation.py
    │           │   │   ├── graph.py
    │           │   │   ├── graphics.py
    │           │   │   ├── graphql.py
    │           │   │   ├── graphviz.py
    │           │   │   ├── gsql.py
    │           │   │   ├── hare.py
    │           │   │   ├── haskell.py
    │           │   │   ├── haxe.py
    │           │   │   ├── hdl.py
    │           │   │   ├── hexdump.py
    │           │   │   ├── html.py
    │           │   │   ├── idl.py
    │           │   │   ├── igor.py
    │           │   │   ├── inferno.py
    │           │   │   ├── installers.py
    │           │   │   ├── int_fiction.py
    │           │   │   ├── iolang.py
    │           │   │   ├── j.py
    │           │   │   ├── javascript.py
    │           │   │   ├── jmespath.py
    │           │   │   ├── jslt.py
    │           │   │   ├── json5.py
    │           │   │   ├── jsonnet.py
    │           │   │   ├── jsx.py
    │           │   │   ├── julia.py
    │           │   │   ├── jvm.py
    │           │   │   ├── kuin.py
    │           │   │   ├── kusto.py
    │           │   │   ├── ldap.py
    │           │   │   ├── lean.py
    │           │   │   ├── lilypond.py
    │           │   │   ├── lisp.py
    │           │   │   ├── macaulay2.py
    │           │   │   ├── make.py
    │           │   │   ├── maple.py
    │           │   │   ├── markup.py
    │           │   │   ├── math.py
    │           │   │   ├── matlab.py
    │           │   │   ├── maxima.py
    │           │   │   ├── meson.py
    │           │   │   ├── mime.py
    │           │   │   ├── minecraft.py
    │           │   │   ├── mips.py
    │           │   │   ├── ml.py
    │           │   │   ├── modeling.py
    │           │   │   ├── modula2.py
    │           │   │   ├── mojo.py
    │           │   │   ├── monte.py
    │           │   │   ├── mosel.py
    │           │   │   ├── ncl.py
    │           │   │   ├── nimrod.py
    │           │   │   ├── nit.py
    │           │   │   ├── nix.py
    │           │   │   ├── numbair.py
    │           │   │   ├── oberon.py
    │           │   │   ├── objective.py
    │           │   │   ├── ooc.py
    │           │   │   ├── openscad.py
    │           │   │   ├── other.py
    │           │   │   ├── parasail.py
    │           │   │   ├── parsers.py
    │           │   │   ├── pascal.py
    │           │   │   ├── pawn.py
    │           │   │   ├── pddl.py
    │           │   │   ├── perl.py
    │           │   │   ├── phix.py
    │           │   │   ├── php.py
    │           │   │   ├── pointless.py
    │           │   │   ├── pony.py
    │           │   │   ├── praat.py
    │           │   │   ├── procfile.py
    │           │   │   ├── prolog.py
    │           │   │   ├── promql.py
    │           │   │   ├── prql.py
    │           │   │   ├── ptx.py
    │           │   │   ├── python.py
    │           │   │   ├── q.py
    │           │   │   ├── qlik.py
    │           │   │   ├── qvt.py
    │           │   │   ├── r.py
    │           │   │   ├── rdf.py
    │           │   │   ├── rebol.py
    │           │   │   ├── rego.py
    │           │   │   ├── resource.py
    │           │   │   ├── ride.py
    │           │   │   ├── rita.py
    │           │   │   ├── rnc.py
    │           │   │   ├── roboconf.py
    │           │   │   ├── robotframework.py
    │           │   │   ├── ruby.py
    │           │   │   ├── rust.py
    │           │   │   ├── sas.py
    │           │   │   ├── savi.py
    │           │   │   ├── scdoc.py
    │           │   │   ├── scripting.py
    │           │   │   ├── sgf.py
    │           │   │   ├── shell.py
    │           │   │   ├── sieve.py
    │           │   │   ├── slash.py
    │           │   │   ├── smalltalk.py
    │           │   │   ├── smithy.py
    │           │   │   ├── smv.py
    │           │   │   ├── snobol.py
    │           │   │   ├── solidity.py
    │           │   │   ├── soong.py
    │           │   │   ├── sophia.py
    │           │   │   ├── special.py
    │           │   │   ├── spice.py
    │           │   │   ├── sql.py
    │           │   │   ├── srcinfo.py
    │           │   │   ├── stata.py
    │           │   │   ├── supercollider.py
    │           │   │   ├── tablegen.py
    │           │   │   ├── tact.py
    │           │   │   ├── tal.py
    │           │   │   ├── tcl.py
    │           │   │   ├── teal.py
    │           │   │   ├── templates.py
    │           │   │   ├── teraterm.py
    │           │   │   ├── testing.py
    │           │   │   ├── text.py
    │           │   │   ├── textedit.py
    │           │   │   ├── textfmts.py
    │           │   │   ├── theorem.py
    │           │   │   ├── thingsdb.py
    │           │   │   ├── tlb.py
    │           │   │   ├── tls.py
    │           │   │   ├── tnt.py
    │           │   │   ├── trafficscript.py
    │           │   │   ├── typoscript.py
    │           │   │   ├── typst.py
    │           │   │   ├── ul4.py
    │           │   │   ├── unicon.py
    │           │   │   ├── urbi.py
    │           │   │   ├── usd.py
    │           │   │   ├── varnish.py
    │           │   │   ├── verification.py
    │           │   │   ├── verifpal.py
    │           │   │   ├── vip.py
    │           │   │   ├── vyper.py
    │           │   │   ├── web.py
    │           │   │   ├── webassembly.py
    │           │   │   ├── webidl.py
    │           │   │   ├── webmisc.py
    │           │   │   ├── wgsl.py
    │           │   │   ├── whiley.py
    │           │   │   ├── wowtoc.py
    │           │   │   ├── wren.py
    │           │   │   ├── x10.py
    │           │   │   ├── xorg.py
    │           │   │   ├── yang.py
    │           │   │   ├── yara.py
    │           │   │   └── zig.py
    │           │   ├── modeline.py
    │           │   ├── plugin.py
    │           │   ├── regexopt.py
    │           │   ├── scanner.py
    │           │   ├── sphinxext.py
    │           │   ├── style.py
    │           │   ├── styles
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── _mapping.cpython-310.pyc
    │           │   │   │   ├── abap.cpython-310.pyc
    │           │   │   │   ├── algol.cpython-310.pyc
    │           │   │   │   ├── algol_nu.cpython-310.pyc
    │           │   │   │   ├── arduino.cpython-310.pyc
    │           │   │   │   ├── autumn.cpython-310.pyc
    │           │   │   │   ├── borland.cpython-310.pyc
    │           │   │   │   ├── bw.cpython-310.pyc
    │           │   │   │   ├── coffee.cpython-310.pyc
    │           │   │   │   ├── colorful.cpython-310.pyc
    │           │   │   │   ├── default.cpython-310.pyc
    │           │   │   │   ├── dracula.cpython-310.pyc
    │           │   │   │   ├── emacs.cpython-310.pyc
    │           │   │   │   ├── friendly.cpython-310.pyc
    │           │   │   │   ├── friendly_grayscale.cpython-310.pyc
    │           │   │   │   ├── fruity.cpython-310.pyc
    │           │   │   │   ├── gh_dark.cpython-310.pyc
    │           │   │   │   ├── gruvbox.cpython-310.pyc
    │           │   │   │   ├── igor.cpython-310.pyc
    │           │   │   │   ├── inkpot.cpython-310.pyc
    │           │   │   │   ├── lightbulb.cpython-310.pyc
    │           │   │   │   ├── lilypond.cpython-310.pyc
    │           │   │   │   ├── lovelace.cpython-310.pyc
    │           │   │   │   ├── manni.cpython-310.pyc
    │           │   │   │   ├── material.cpython-310.pyc
    │           │   │   │   ├── monokai.cpython-310.pyc
    │           │   │   │   ├── murphy.cpython-310.pyc
    │           │   │   │   ├── native.cpython-310.pyc
    │           │   │   │   ├── nord.cpython-310.pyc
    │           │   │   │   ├── onedark.cpython-310.pyc
    │           │   │   │   ├── paraiso_dark.cpython-310.pyc
    │           │   │   │   ├── paraiso_light.cpython-310.pyc
    │           │   │   │   ├── pastie.cpython-310.pyc
    │           │   │   │   ├── perldoc.cpython-310.pyc
    │           │   │   │   ├── rainbow_dash.cpython-310.pyc
    │           │   │   │   ├── rrt.cpython-310.pyc
    │           │   │   │   ├── sas.cpython-310.pyc
    │           │   │   │   ├── solarized.cpython-310.pyc
    │           │   │   │   ├── staroffice.cpython-310.pyc
    │           │   │   │   ├── stata_dark.cpython-310.pyc
    │           │   │   │   ├── stata_light.cpython-310.pyc
    │           │   │   │   ├── tango.cpython-310.pyc
    │           │   │   │   ├── trac.cpython-310.pyc
    │           │   │   │   ├── vim.cpython-310.pyc
    │           │   │   │   ├── vs.cpython-310.pyc
    │           │   │   │   ├── xcode.cpython-310.pyc
    │           │   │   │   └── zenburn.cpython-310.pyc
    │           │   │   ├── _mapping.py
    │           │   │   ├── abap.py
    │           │   │   ├── algol.py
    │           │   │   ├── algol_nu.py
    │           │   │   ├── arduino.py
    │           │   │   ├── autumn.py
    │           │   │   ├── borland.py
    │           │   │   ├── bw.py
    │           │   │   ├── coffee.py
    │           │   │   ├── colorful.py
    │           │   │   ├── default.py
    │           │   │   ├── dracula.py
    │           │   │   ├── emacs.py
    │           │   │   ├── friendly.py
    │           │   │   ├── friendly_grayscale.py
    │           │   │   ├── fruity.py
    │           │   │   ├── gh_dark.py
    │           │   │   ├── gruvbox.py
    │           │   │   ├── igor.py
    │           │   │   ├── inkpot.py
    │           │   │   ├── lightbulb.py
    │           │   │   ├── lilypond.py
    │           │   │   ├── lovelace.py
    │           │   │   ├── manni.py
    │           │   │   ├── material.py
    │           │   │   ├── monokai.py
    │           │   │   ├── murphy.py
    │           │   │   ├── native.py
    │           │   │   ├── nord.py
    │           │   │   ├── onedark.py
    │           │   │   ├── paraiso_dark.py
    │           │   │   ├── paraiso_light.py
    │           │   │   ├── pastie.py
    │           │   │   ├── perldoc.py
    │           │   │   ├── rainbow_dash.py
    │           │   │   ├── rrt.py
    │           │   │   ├── sas.py
    │           │   │   ├── solarized.py
    │           │   │   ├── staroffice.py
    │           │   │   ├── stata_dark.py
    │           │   │   ├── stata_light.py
    │           │   │   ├── tango.py
    │           │   │   ├── trac.py
    │           │   │   ├── vim.py
    │           │   │   ├── vs.py
    │           │   │   ├── xcode.py
    │           │   │   └── zenburn.py
    │           │   ├── token.py
    │           │   ├── unistring.py
    │           │   └── util.py
    │           ├── pygments-2.19.2.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   ├── entry_points.txt
    │           │   └── licenses
    │           │       ├── AUTHORS
    │           │       └── LICENSE
    │           ├── pyyaml-6.0.3.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── REQUESTED
    │           │   ├── WHEEL
    │           │   ├── licenses
    │           │   │   └── LICENSE
    │           │   └── top_level.txt
    │           ├── rich
    │           │   ├── __init__.py
    │           │   ├── __main__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── __main__.cpython-310.pyc
    │           │   │   ├── _emoji_codes.cpython-310.pyc
    │           │   │   ├── _emoji_replace.cpython-310.pyc
    │           │   │   ├── _export_format.cpython-310.pyc
    │           │   │   ├── _extension.cpython-310.pyc
    │           │   │   ├── _fileno.cpython-310.pyc
    │           │   │   ├── _inspect.cpython-310.pyc
    │           │   │   ├── _log_render.cpython-310.pyc
    │           │   │   ├── _loop.cpython-310.pyc
    │           │   │   ├── _null_file.cpython-310.pyc
    │           │   │   ├── _palettes.cpython-310.pyc
    │           │   │   ├── _pick.cpython-310.pyc
    │           │   │   ├── _ratio.cpython-310.pyc
    │           │   │   ├── _spinners.cpython-310.pyc
    │           │   │   ├── _stack.cpython-310.pyc
    │           │   │   ├── _timer.cpython-310.pyc
    │           │   │   ├── _win32_console.cpython-310.pyc
    │           │   │   ├── _windows.cpython-310.pyc
    │           │   │   ├── _windows_renderer.cpython-310.pyc
    │           │   │   ├── _wrap.cpython-310.pyc
    │           │   │   ├── abc.cpython-310.pyc
    │           │   │   ├── align.cpython-310.pyc
    │           │   │   ├── ansi.cpython-310.pyc
    │           │   │   ├── bar.cpython-310.pyc
    │           │   │   ├── box.cpython-310.pyc
    │           │   │   ├── cells.cpython-310.pyc
    │           │   │   ├── color.cpython-310.pyc
    │           │   │   ├── color_triplet.cpython-310.pyc
    │           │   │   ├── columns.cpython-310.pyc
    │           │   │   ├── console.cpython-310.pyc
    │           │   │   ├── constrain.cpython-310.pyc
    │           │   │   ├── containers.cpython-310.pyc
    │           │   │   ├── control.cpython-310.pyc
    │           │   │   ├── default_styles.cpython-310.pyc
    │           │   │   ├── diagnose.cpython-310.pyc
    │           │   │   ├── emoji.cpython-310.pyc
    │           │   │   ├── errors.cpython-310.pyc
    │           │   │   ├── file_proxy.cpython-310.pyc
    │           │   │   ├── filesize.cpython-310.pyc
    │           │   │   ├── highlighter.cpython-310.pyc
    │           │   │   ├── json.cpython-310.pyc
    │           │   │   ├── jupyter.cpython-310.pyc
    │           │   │   ├── layout.cpython-310.pyc
    │           │   │   ├── live.cpython-310.pyc
    │           │   │   ├── live_render.cpython-310.pyc
    │           │   │   ├── logging.cpython-310.pyc
    │           │   │   ├── markdown.cpython-310.pyc
    │           │   │   ├── markup.cpython-310.pyc
    │           │   │   ├── measure.cpython-310.pyc
    │           │   │   ├── padding.cpython-310.pyc
    │           │   │   ├── pager.cpython-310.pyc
    │           │   │   ├── palette.cpython-310.pyc
    │           │   │   ├── panel.cpython-310.pyc
    │           │   │   ├── pretty.cpython-310.pyc
    │           │   │   ├── progress.cpython-310.pyc
    │           │   │   ├── progress_bar.cpython-310.pyc
    │           │   │   ├── prompt.cpython-310.pyc
    │           │   │   ├── protocol.cpython-310.pyc
    │           │   │   ├── region.cpython-310.pyc
    │           │   │   ├── repr.cpython-310.pyc
    │           │   │   ├── rule.cpython-310.pyc
    │           │   │   ├── scope.cpython-310.pyc
    │           │   │   ├── screen.cpython-310.pyc
    │           │   │   ├── segment.cpython-310.pyc
    │           │   │   ├── spinner.cpython-310.pyc
    │           │   │   ├── status.cpython-310.pyc
    │           │   │   ├── style.cpython-310.pyc
    │           │   │   ├── styled.cpython-310.pyc
    │           │   │   ├── syntax.cpython-310.pyc
    │           │   │   ├── table.cpython-310.pyc
    │           │   │   ├── terminal_theme.cpython-310.pyc
    │           │   │   ├── text.cpython-310.pyc
    │           │   │   ├── theme.cpython-310.pyc
    │           │   │   ├── themes.cpython-310.pyc
    │           │   │   ├── traceback.cpython-310.pyc
    │           │   │   └── tree.cpython-310.pyc
    │           │   ├── _emoji_codes.py
    │           │   ├── _emoji_replace.py
    │           │   ├── _export_format.py
    │           │   ├── _extension.py
    │           │   ├── _fileno.py
    │           │   ├── _inspect.py
    │           │   ├── _log_render.py
    │           │   ├── _loop.py
    │           │   ├── _null_file.py
    │           │   ├── _palettes.py
    │           │   ├── _pick.py
    │           │   ├── _ratio.py
    │           │   ├── _spinners.py
    │           │   ├── _stack.py
    │           │   ├── _timer.py
    │           │   ├── _unicode_data
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── _versions.cpython-310.pyc
    │           │   │   │   ├── unicode10-0-0.cpython-310.pyc
    │           │   │   │   ├── unicode11-0-0.cpython-310.pyc
    │           │   │   │   ├── unicode12-0-0.cpython-310.pyc
    │           │   │   │   ├── unicode12-1-0.cpython-310.pyc
    │           │   │   │   ├── unicode13-0-0.cpython-310.pyc
    │           │   │   │   ├── unicode14-0-0.cpython-310.pyc
    │           │   │   │   ├── unicode15-0-0.cpython-310.pyc
    │           │   │   │   ├── unicode15-1-0.cpython-310.pyc
    │           │   │   │   ├── unicode16-0-0.cpython-310.pyc
    │           │   │   │   ├── unicode17-0-0.cpython-310.pyc
    │           │   │   │   ├── unicode4-1-0.cpython-310.pyc
    │           │   │   │   ├── unicode5-0-0.cpython-310.pyc
    │           │   │   │   ├── unicode5-1-0.cpython-310.pyc
    │           │   │   │   ├── unicode5-2-0.cpython-310.pyc
    │           │   │   │   ├── unicode6-0-0.cpython-310.pyc
    │           │   │   │   ├── unicode6-1-0.cpython-310.pyc
    │           │   │   │   ├── unicode6-2-0.cpython-310.pyc
    │           │   │   │   ├── unicode6-3-0.cpython-310.pyc
    │           │   │   │   ├── unicode7-0-0.cpython-310.pyc
    │           │   │   │   ├── unicode8-0-0.cpython-310.pyc
    │           │   │   │   └── unicode9-0-0.cpython-310.pyc
    │           │   │   ├── _versions.py
    │           │   │   ├── unicode10-0-0.py
    │           │   │   ├── unicode11-0-0.py
    │           │   │   ├── unicode12-0-0.py
    │           │   │   ├── unicode12-1-0.py
    │           │   │   ├── unicode13-0-0.py
    │           │   │   ├── unicode14-0-0.py
    │           │   │   ├── unicode15-0-0.py
    │           │   │   ├── unicode15-1-0.py
    │           │   │   ├── unicode16-0-0.py
    │           │   │   ├── unicode17-0-0.py
    │           │   │   ├── unicode4-1-0.py
    │           │   │   ├── unicode5-0-0.py
    │           │   │   ├── unicode5-1-0.py
    │           │   │   ├── unicode5-2-0.py
    │           │   │   ├── unicode6-0-0.py
    │           │   │   ├── unicode6-1-0.py
    │           │   │   ├── unicode6-2-0.py
    │           │   │   ├── unicode6-3-0.py
    │           │   │   ├── unicode7-0-0.py
    │           │   │   ├── unicode8-0-0.py
    │           │   │   └── unicode9-0-0.py
    │           │   ├── _win32_console.py
    │           │   ├── _windows.py
    │           │   ├── _windows_renderer.py
    │           │   ├── _wrap.py
    │           │   ├── abc.py
    │           │   ├── align.py
    │           │   ├── ansi.py
    │           │   ├── bar.py
    │           │   ├── box.py
    │           │   ├── cells.py
    │           │   ├── color.py
    │           │   ├── color_triplet.py
    │           │   ├── columns.py
    │           │   ├── console.py
    │           │   ├── constrain.py
    │           │   ├── containers.py
    │           │   ├── control.py
    │           │   ├── default_styles.py
    │           │   ├── diagnose.py
    │           │   ├── emoji.py
    │           │   ├── errors.py
    │           │   ├── file_proxy.py
    │           │   ├── filesize.py
    │           │   ├── highlighter.py
    │           │   ├── json.py
    │           │   ├── jupyter.py
    │           │   ├── layout.py
    │           │   ├── live.py
    │           │   ├── live_render.py
    │           │   ├── logging.py
    │           │   ├── markdown.py
    │           │   ├── markup.py
    │           │   ├── measure.py
    │           │   ├── padding.py
    │           │   ├── pager.py
    │           │   ├── palette.py
    │           │   ├── panel.py
    │           │   ├── pretty.py
    │           │   ├── progress.py
    │           │   ├── progress_bar.py
    │           │   ├── prompt.py
    │           │   ├── protocol.py
    │           │   ├── py.typed
    │           │   ├── region.py
    │           │   ├── repr.py
    │           │   ├── rule.py
    │           │   ├── scope.py
    │           │   ├── screen.py
    │           │   ├── segment.py
    │           │   ├── spinner.py
    │           │   ├── status.py
    │           │   ├── style.py
    │           │   ├── styled.py
    │           │   ├── syntax.py
    │           │   ├── table.py
    │           │   ├── terminal_theme.py
    │           │   ├── text.py
    │           │   ├── theme.py
    │           │   ├── themes.py
    │           │   ├── traceback.py
    │           │   └── tree.py
    │           ├── rich-14.3.3.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   └── licenses
    │           │       └── LICENSE
    │           ├── setuptools
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── _deprecation_warning.cpython-310.pyc
    │           │   │   ├── _imp.cpython-310.pyc
    │           │   │   ├── archive_util.cpython-310.pyc
    │           │   │   ├── build_meta.cpython-310.pyc
    │           │   │   ├── config.cpython-310.pyc
    │           │   │   ├── dep_util.cpython-310.pyc
    │           │   │   ├── depends.cpython-310.pyc
    │           │   │   ├── dist.cpython-310.pyc
    │           │   │   ├── errors.cpython-310.pyc
    │           │   │   ├── extension.cpython-310.pyc
    │           │   │   ├── glob.cpython-310.pyc
    │           │   │   ├── installer.cpython-310.pyc
    │           │   │   ├── launch.cpython-310.pyc
    │           │   │   ├── monkey.cpython-310.pyc
    │           │   │   ├── msvc.cpython-310.pyc
    │           │   │   ├── namespaces.cpython-310.pyc
    │           │   │   ├── package_index.cpython-310.pyc
    │           │   │   ├── py34compat.cpython-310.pyc
    │           │   │   ├── sandbox.cpython-310.pyc
    │           │   │   ├── unicode_utils.cpython-310.pyc
    │           │   │   ├── version.cpython-310.pyc
    │           │   │   ├── wheel.cpython-310.pyc
    │           │   │   └── windows_support.cpython-310.pyc
    │           │   ├── _deprecation_warning.py
    │           │   ├── _distutils
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── _msvccompiler.cpython-310.pyc
    │           │   │   │   ├── archive_util.cpython-310.pyc
    │           │   │   │   ├── bcppcompiler.cpython-310.pyc
    │           │   │   │   ├── ccompiler.cpython-310.pyc
    │           │   │   │   ├── cmd.cpython-310.pyc
    │           │   │   │   ├── config.cpython-310.pyc
    │           │   │   │   ├── core.cpython-310.pyc
    │           │   │   │   ├── cygwinccompiler.cpython-310.pyc
    │           │   │   │   ├── debug.cpython-310.pyc
    │           │   │   │   ├── dep_util.cpython-310.pyc
    │           │   │   │   ├── dir_util.cpython-310.pyc
    │           │   │   │   ├── dist.cpython-310.pyc
    │           │   │   │   ├── errors.cpython-310.pyc
    │           │   │   │   ├── extension.cpython-310.pyc
    │           │   │   │   ├── fancy_getopt.cpython-310.pyc
    │           │   │   │   ├── file_util.cpython-310.pyc
    │           │   │   │   ├── filelist.cpython-310.pyc
    │           │   │   │   ├── log.cpython-310.pyc
    │           │   │   │   ├── msvc9compiler.cpython-310.pyc
    │           │   │   │   ├── msvccompiler.cpython-310.pyc
    │           │   │   │   ├── py35compat.cpython-310.pyc
    │           │   │   │   ├── py38compat.cpython-310.pyc
    │           │   │   │   ├── spawn.cpython-310.pyc
    │           │   │   │   ├── sysconfig.cpython-310.pyc
    │           │   │   │   ├── text_file.cpython-310.pyc
    │           │   │   │   ├── unixccompiler.cpython-310.pyc
    │           │   │   │   ├── util.cpython-310.pyc
    │           │   │   │   ├── version.cpython-310.pyc
    │           │   │   │   └── versionpredicate.cpython-310.pyc
    │           │   │   ├── _msvccompiler.py
    │           │   │   ├── archive_util.py
    │           │   │   ├── bcppcompiler.py
    │           │   │   ├── ccompiler.py
    │           │   │   ├── cmd.py
    │           │   │   ├── command
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── bdist.cpython-310.pyc
    │           │   │   │   │   ├── bdist_dumb.cpython-310.pyc
    │           │   │   │   │   ├── bdist_msi.cpython-310.pyc
    │           │   │   │   │   ├── bdist_rpm.cpython-310.pyc
    │           │   │   │   │   ├── bdist_wininst.cpython-310.pyc
    │           │   │   │   │   ├── build.cpython-310.pyc
    │           │   │   │   │   ├── build_clib.cpython-310.pyc
    │           │   │   │   │   ├── build_ext.cpython-310.pyc
    │           │   │   │   │   ├── build_py.cpython-310.pyc
    │           │   │   │   │   ├── build_scripts.cpython-310.pyc
    │           │   │   │   │   ├── check.cpython-310.pyc
    │           │   │   │   │   ├── clean.cpython-310.pyc
    │           │   │   │   │   ├── config.cpython-310.pyc
    │           │   │   │   │   ├── install.cpython-310.pyc
    │           │   │   │   │   ├── install_data.cpython-310.pyc
    │           │   │   │   │   ├── install_egg_info.cpython-310.pyc
    │           │   │   │   │   ├── install_headers.cpython-310.pyc
    │           │   │   │   │   ├── install_lib.cpython-310.pyc
    │           │   │   │   │   ├── install_scripts.cpython-310.pyc
    │           │   │   │   │   ├── py37compat.cpython-310.pyc
    │           │   │   │   │   ├── register.cpython-310.pyc
    │           │   │   │   │   ├── sdist.cpython-310.pyc
    │           │   │   │   │   └── upload.cpython-310.pyc
    │           │   │   │   ├── bdist.py
    │           │   │   │   ├── bdist_dumb.py
    │           │   │   │   ├── bdist_msi.py
    │           │   │   │   ├── bdist_rpm.py
    │           │   │   │   ├── bdist_wininst.py
    │           │   │   │   ├── build.py
    │           │   │   │   ├── build_clib.py
    │           │   │   │   ├── build_ext.py
    │           │   │   │   ├── build_py.py
    │           │   │   │   ├── build_scripts.py
    │           │   │   │   ├── check.py
    │           │   │   │   ├── clean.py
    │           │   │   │   ├── config.py
    │           │   │   │   ├── install.py
    │           │   │   │   ├── install_data.py
    │           │   │   │   ├── install_egg_info.py
    │           │   │   │   ├── install_headers.py
    │           │   │   │   ├── install_lib.py
    │           │   │   │   ├── install_scripts.py
    │           │   │   │   ├── py37compat.py
    │           │   │   │   ├── register.py
    │           │   │   │   ├── sdist.py
    │           │   │   │   └── upload.py
    │           │   │   ├── config.py
    │           │   │   ├── core.py
    │           │   │   ├── cygwinccompiler.py
    │           │   │   ├── debug.py
    │           │   │   ├── dep_util.py
    │           │   │   ├── dir_util.py
    │           │   │   ├── dist.py
    │           │   │   ├── errors.py
    │           │   │   ├── extension.py
    │           │   │   ├── fancy_getopt.py
    │           │   │   ├── file_util.py
    │           │   │   ├── filelist.py
    │           │   │   ├── log.py
    │           │   │   ├── msvc9compiler.py
    │           │   │   ├── msvccompiler.py
    │           │   │   ├── py35compat.py
    │           │   │   ├── py38compat.py
    │           │   │   ├── spawn.py
    │           │   │   ├── sysconfig.py
    │           │   │   ├── text_file.py
    │           │   │   ├── unixccompiler.py
    │           │   │   ├── util.py
    │           │   │   ├── version.py
    │           │   │   └── versionpredicate.py
    │           │   ├── _imp.py
    │           │   ├── _vendor
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── ordered_set.cpython-310.pyc
    │           │   │   │   └── pyparsing.cpython-310.pyc
    │           │   │   ├── more_itertools
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── more.cpython-310.pyc
    │           │   │   │   │   └── recipes.cpython-310.pyc
    │           │   │   │   ├── more.py
    │           │   │   │   └── recipes.py
    │           │   │   ├── ordered_set.py
    │           │   │   ├── packaging
    │           │   │   │   ├── __about__.py
    │           │   │   │   ├── __init__.py
    │           │   │   │   ├── __pycache__
    │           │   │   │   │   ├── __about__.cpython-310.pyc
    │           │   │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   │   ├── _manylinux.cpython-310.pyc
    │           │   │   │   │   ├── _musllinux.cpython-310.pyc
    │           │   │   │   │   ├── _structures.cpython-310.pyc
    │           │   │   │   │   ├── markers.cpython-310.pyc
    │           │   │   │   │   ├── requirements.cpython-310.pyc
    │           │   │   │   │   ├── specifiers.cpython-310.pyc
    │           │   │   │   │   ├── tags.cpython-310.pyc
    │           │   │   │   │   ├── utils.cpython-310.pyc
    │           │   │   │   │   └── version.cpython-310.pyc
    │           │   │   │   ├── _manylinux.py
    │           │   │   │   ├── _musllinux.py
    │           │   │   │   ├── _structures.py
    │           │   │   │   ├── markers.py
    │           │   │   │   ├── requirements.py
    │           │   │   │   ├── specifiers.py
    │           │   │   │   ├── tags.py
    │           │   │   │   ├── utils.py
    │           │   │   │   └── version.py
    │           │   │   └── pyparsing.py
    │           │   ├── archive_util.py
    │           │   ├── build_meta.py
    │           │   ├── cli-32.exe
    │           │   ├── cli-64.exe
    │           │   ├── cli-arm64.exe
    │           │   ├── cli.exe
    │           │   ├── command
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── alias.cpython-310.pyc
    │           │   │   │   ├── bdist_egg.cpython-310.pyc
    │           │   │   │   ├── bdist_rpm.cpython-310.pyc
    │           │   │   │   ├── build_clib.cpython-310.pyc
    │           │   │   │   ├── build_ext.cpython-310.pyc
    │           │   │   │   ├── build_py.cpython-310.pyc
    │           │   │   │   ├── develop.cpython-310.pyc
    │           │   │   │   ├── dist_info.cpython-310.pyc
    │           │   │   │   ├── easy_install.cpython-310.pyc
    │           │   │   │   ├── egg_info.cpython-310.pyc
    │           │   │   │   ├── install.cpython-310.pyc
    │           │   │   │   ├── install_egg_info.cpython-310.pyc
    │           │   │   │   ├── install_lib.cpython-310.pyc
    │           │   │   │   ├── install_scripts.cpython-310.pyc
    │           │   │   │   ├── py36compat.cpython-310.pyc
    │           │   │   │   ├── register.cpython-310.pyc
    │           │   │   │   ├── rotate.cpython-310.pyc
    │           │   │   │   ├── saveopts.cpython-310.pyc
    │           │   │   │   ├── sdist.cpython-310.pyc
    │           │   │   │   ├── setopt.cpython-310.pyc
    │           │   │   │   ├── test.cpython-310.pyc
    │           │   │   │   ├── upload.cpython-310.pyc
    │           │   │   │   └── upload_docs.cpython-310.pyc
    │           │   │   ├── alias.py
    │           │   │   ├── bdist_egg.py
    │           │   │   ├── bdist_rpm.py
    │           │   │   ├── build_clib.py
    │           │   │   ├── build_ext.py
    │           │   │   ├── build_py.py
    │           │   │   ├── develop.py
    │           │   │   ├── dist_info.py
    │           │   │   ├── easy_install.py
    │           │   │   ├── egg_info.py
    │           │   │   ├── install.py
    │           │   │   ├── install_egg_info.py
    │           │   │   ├── install_lib.py
    │           │   │   ├── install_scripts.py
    │           │   │   ├── launcher manifest.xml
    │           │   │   ├── py36compat.py
    │           │   │   ├── register.py
    │           │   │   ├── rotate.py
    │           │   │   ├── saveopts.py
    │           │   │   ├── sdist.py
    │           │   │   ├── setopt.py
    │           │   │   ├── test.py
    │           │   │   ├── upload.py
    │           │   │   └── upload_docs.py
    │           │   ├── config.py
    │           │   ├── dep_util.py
    │           │   ├── depends.py
    │           │   ├── dist.py
    │           │   ├── errors.py
    │           │   ├── extension.py
    │           │   ├── extern
    │           │   │   ├── __init__.py
    │           │   │   └── __pycache__
    │           │   │       └── __init__.cpython-310.pyc
    │           │   ├── glob.py
    │           │   ├── gui-32.exe
    │           │   ├── gui-64.exe
    │           │   ├── gui-arm64.exe
    │           │   ├── gui.exe
    │           │   ├── installer.py
    │           │   ├── launch.py
    │           │   ├── monkey.py
    │           │   ├── msvc.py
    │           │   ├── namespaces.py
    │           │   ├── package_index.py
    │           │   ├── py34compat.py
    │           │   ├── sandbox.py
    │           │   ├── script (dev).tmpl
    │           │   ├── script.tmpl
    │           │   ├── unicode_utils.py
    │           │   ├── version.py
    │           │   ├── wheel.py
    │           │   └── windows_support.py
    │           ├── setuptools-59.6.0.dist-info
    │           │   ├── INSTALLER
    │           │   ├── LICENSE
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── REQUESTED
    │           │   ├── WHEEL
    │           │   ├── entry_points.txt
    │           │   └── top_level.txt
    │           ├── typing_extensions-4.15.0.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── WHEEL
    │           │   └── licenses
    │           │       └── LICENSE
    │           ├── typing_extensions.py
    │           ├── wheel
    │           │   ├── __init__.py
    │           │   ├── __main__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── __main__.cpython-310.pyc
    │           │   │   ├── _bdist_wheel.cpython-310.pyc
    │           │   │   ├── _metadata.cpython-310.pyc
    │           │   │   ├── _setuptools_logging.cpython-310.pyc
    │           │   │   ├── bdist_wheel.cpython-310.pyc
    │           │   │   ├── macosx_libfile.cpython-310.pyc
    │           │   │   ├── metadata.cpython-310.pyc
    │           │   │   └── wheelfile.cpython-310.pyc
    │           │   ├── _bdist_wheel.py
    │           │   ├── _commands
    │           │   │   ├── __init__.py
    │           │   │   ├── __pycache__
    │           │   │   │   ├── __init__.cpython-310.pyc
    │           │   │   │   ├── convert.cpython-310.pyc
    │           │   │   │   ├── pack.cpython-310.pyc
    │           │   │   │   ├── tags.cpython-310.pyc
    │           │   │   │   └── unpack.cpython-310.pyc
    │           │   │   ├── convert.py
    │           │   │   ├── pack.py
    │           │   │   ├── tags.py
    │           │   │   └── unpack.py
    │           │   ├── _metadata.py
    │           │   ├── _setuptools_logging.py
    │           │   ├── bdist_wheel.py
    │           │   ├── macosx_libfile.py
    │           │   ├── metadata.py
    │           │   └── wheelfile.py
    │           ├── wheel-0.46.3.dist-info
    │           │   ├── INSTALLER
    │           │   ├── METADATA
    │           │   ├── RECORD
    │           │   ├── REQUESTED
    │           │   ├── WHEEL
    │           │   ├── entry_points.txt
    │           │   └── licenses
    │           │       └── LICENSE.txt
    │           ├── yaml
    │           │   ├── __init__.py
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   ├── composer.cpython-310.pyc
    │           │   │   ├── constructor.cpython-310.pyc
    │           │   │   ├── cyaml.cpython-310.pyc
    │           │   │   ├── dumper.cpython-310.pyc
    │           │   │   ├── emitter.cpython-310.pyc
    │           │   │   ├── error.cpython-310.pyc
    │           │   │   ├── events.cpython-310.pyc
    │           │   │   ├── loader.cpython-310.pyc
    │           │   │   ├── nodes.cpython-310.pyc
    │           │   │   ├── parser.cpython-310.pyc
    │           │   │   ├── reader.cpython-310.pyc
    │           │   │   ├── representer.cpython-310.pyc
    │           │   │   ├── resolver.cpython-310.pyc
    │           │   │   ├── scanner.cpython-310.pyc
    │           │   │   ├── serializer.cpython-310.pyc
    │           │   │   └── tokens.cpython-310.pyc
    │           │   ├── _yaml.cpython-310-x86_64-linux-gnu.so
    │           │   ├── composer.py
    │           │   ├── constructor.py
    │           │   ├── cyaml.py
    │           │   ├── dumper.py
    │           │   ├── emitter.py
    │           │   ├── error.py
    │           │   ├── events.py
    │           │   ├── loader.py
    │           │   ├── nodes.py
    │           │   ├── parser.py
    │           │   ├── reader.py
    │           │   ├── representer.py
    │           │   ├── resolver.py
    │           │   ├── scanner.py
    │           │   ├── serializer.py
    │           │   └── tokens.py
    │           ├── zstandard
    │           │   ├── __init__.py
    │           │   ├── __init__.pyi
    │           │   ├── __pycache__
    │           │   │   ├── __init__.cpython-310.pyc
    │           │   │   └── backend_cffi.cpython-310.pyc
    │           │   ├── _cffi.cpython-310-x86_64-linux-gnu.so
    │           │   ├── backend_c.cpython-310-x86_64-linux-gnu.so
    │           │   ├── backend_cffi.py
    │           │   └── py.typed
    │           └── zstandard-0.25.0.dist-info
    │               ├── INSTALLER
    │               ├── METADATA
    │               ├── RECORD
    │               ├── WHEEL
    │               ├── licenses
    │               │   └── LICENSE
    │               └── top_level.txt
    ├── lib64 -> lib
    ├── manifest.txt
    └── pyvenv.cfg

400 directories, 3155 files
