##
# Copyright (c) 2009 Piotr Esden-Tempski <piotr@esden.net>
# 
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
# 
# The above copyright notice and this permission notice shall be included in
# all copies or substantial portions of the Software.
# 
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
# THE SOFTWARE.
##

arch_prefix?=arm-none-eabi
compiler_prefix?=${arch_prefix}-

NAME=libcmsis

CC=${compiler_prefix}gcc
AR=${compiler_prefix}ar
AS=${compiler_prefix}as
CFLAGS=-I../include -fno-common -Os -g -mcpu=cortex-m3 -mthumb -ffunction-sections -fdata-sections
ARFLAGS=rcsv
ASFLAGS=-ahls -mapcs-32

objects= core_cm3.o system_stm32.o

all: ${NAME}.a

${NAME}.a: ${objects}
	${AR} ${ARFLAGS} $@ $^

clean:
	rm -rf *.o *.a
