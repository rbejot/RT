# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: hsabouri <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2016/08/19 10:32:42 by hsabouri          #+#    #+#              #
#    Updated: 2017/04/10 16:50:28 by hsabouri         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libmalloc.a
INCLUDES = ./
CFLAGS = -Wall -Werror -Wextra
#CFLAGS += -g -fsanitize=address
CFLAGS += -O3 -march=native
CC = gcc
SRC	= ft_malloc.c ft_memzero.c ft_malloc_other.c
OBJ	= $(SRC:%.c=%.o)

all: $(NAME)

$(NAME): $(OBJ)
	ar rcs $@ $^
	ranlib $@

%.o: %.c
	$(CC) $(CFLAGS) -c -o $@ $< -I$(INCLUDES)

clean:
	rm -f $(OBJ)

fclean: clean
	rm -f $(NAME)

re: fclean
	$(MAKE) all
