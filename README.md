<<<<<<< HEAD
# 计算机组成原理课程设计——使用微程序控制器实现的模型机
---

## 功能介绍
该模型机采用微程序控制的方式，实现加、减、乘、除、逻辑移位、与、或、非、异或等基本运算指令，load/store指令，条件跳转和无条件跳转指令。具体功能介绍请见`"计算机组成原理与设计报告.pdf"`

## 环境依赖
1.Win7

2.Quartus II 13.0(sp1 64bit)

3.FPGA开发版(Cyclone IV E EP4CE6E22C8)

## 部署步骤
1. 安装Quartus II 13.0软件，并且将FPGA开发板配置好,通过USB接口等连接到电脑上

2. 将`Micro_Programming`目录复制到任一**英文**路径下(注意一定是英文路径，否则Quartus运行会不正常), 双击打开`Micro_Programming.qpf`工程文件， 然后再打开`Project Navigator`（`Alt+0`）,双击打开`Micro_Programming.bsf`文件便可以查看设计图
![打开工程文件`Micro_Programming.qpf`](image/open.jpg ''fig_1'')


3. 编译工程文件:选择菜单栏`Processing > Start Compilation`(`Ctrl+L`)编译该工程，然后选择菜单栏`Assignment > Pin Planner`分配管脚， 最后选择`Tools > Programmer > Start`将编译好的文件下载到FPGA开发板上

注： 对于第一次学习使用Quartus的人士，之后会上传一份详细的使用说明


## 目录结构描述
MicroProgramming
    C:.
│  3mux1_16.bdf
│  3mux1_16.bsf
│  ALU.bdf
│  ALU.bsf
│  div.bsf
│  div.cmp
│  div.qip
│  div.vhd
│  err_info.txt
│  err_reading.txt
│  houji.bdf
│  houji.bsf
│  Micro_Programming.bdf
│  Micro_Programming.qpf
│  Micro_Programming.qsf
│  Micro_Programming.qws
│  Micro_Programming_assignment_defaults.qdf
│  mult.bsf
│  mult.cmp
│  mult.qip
│  mult.vhd
│  mux16.bdf
│  mux16.bsf
│  mux2.bdf
│  mux2.bsf
│  mux3.bdf
│  mux3.bsf
│  On_Off.bdf
│  On_Off.bsf
│  RAM.bsf
│  RAM.cmp
│  ram.mif
│  RAM.qip
│  RAM.vhd
│  Reg16.bdf
│  Reg16.bsf
│  ROM.bsf
│  ROM.cmp
│  rom.mif
│  ROM.qip
│  ROM.vhd
│  rom_nextadd.bsf
│  rom_nextadd.cmp
│  rom_nextadd.qip
│  rom_nextadd.vhd
│  rom_Nextaddr.mif
│  treefile.md
│  treefile.txt
│  uPC.bdf
│  uPC.bsf
│  
├─db
│      .cmp.kpt
│      add_sub_7pc.tdf
│      add_sub_8pc.tdf
│      altsyncram_18v3.tdf
│      altsyncram_7nc1.tdf
│      altsyncram_a8e2.tdf
│      altsyncram_cos2.tdf
│      altsyncram_p5v3.tdf
│      altsyncram_pad2.tdf
│      altsyncram_rmb1.tdf
│      altsyncram_sss2.tdf
│      alt_u_div_h7f.tdf
│      decode_k8a.tdf
│      decode_rsa.tdf
│      logic_util_heursitic.dat
│      lpm_divide_m6r.tdf
│      Micro_Programming.db_info
│      Micro_Programming.ipinfo
│      Micro_Programming.sld_design_entry.sci
│      mult_t5n.tdf
│      mux_qob.tdf
│      prev_cmp_Micro_Programming.qmsg
│      sign_div_unsign_p7h.tdf
│      
├─greybox_tmp
│  │  cbx_args.txt
│  │  
│  └─greybox_tmp
├─incremental_db
│  │  README
│  │  
│  └─compiled_partitions
│          Micro_Programming.db_info
│          
├─output_files
│  │  Micro_Programming.asm.rpt
│  │  Micro_Programming.done
│  │  Micro_Programming.eda.rpt
│  │  Micro_Programming.fit.rpt
│  │  Micro_Programming.fit.smsg
│  │  Micro_Programming.fit.summary
│  │  Micro_Programming.flow.rpt
│  │  Micro_Programming.jdi
│  │  Micro_Programming.map.rpt
│  │  Micro_Programming.map.summary
│  │  Micro_Programming.pin
│  │  Micro_Programming.sof
│  │  Micro_Programming.sta.rpt
│  │  Micro_Programming.sta.summary
│  │  RAM.qip
│  │  rom.qip
│  │  rom_nextadd.qip
│  │  
│  ├─greybox_tmp
│  │      cbx_args.txt
│  │      
│  └─output_files
│          Chain4.cdf
│          
└─simulation
    └─modelsim
            Micro_Programming.sft
            Micro_Programming.vho
            Micro_Programming_8_1200mv_0c_slow.vho
            Micro_Programming_8_1200mv_0c_vhd_slow.sdo
            Micro_Programming_8_1200mv_85c_slow.vho
            Micro_Programming_8_1200mv_85c_vhd_slow.sdo
            Micro_Programming_min_1200mv_0c_fast.vho
            Micro_Programming_min_1200mv_0c_vhd_fast.sdo
            Micro_Programming_modelsim.xrf
            Micro_Programming_vhd.sdo



##版本

V1.0

##Contact &  Copyright

作者:zhangzw12319

邮箱:zhangzw12319@163.com

模型机MicroProgramming文件夹内文件在Apache License 2协议下发布，允许代码修改，再发布(作为开源或商业软件),但是如果你修改了代码，需要在被修改的文件中说明，并且再次发布修改或未修改版本时需要带上Apache License 2协议.

Notice:项目中`计算机组成原理与设计报告.pdf`文件未经作者授权许可不得装载或修改;如需使用请邮件联系原作者，并且再取得许可后注明来源于出处。感谢您的支持与理解。

