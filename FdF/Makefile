# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: bmuselet <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2017/11/28 15:19:34 by bmuselet          #+#    #+#              #
#    Updated: 2018/01/11 11:16:44 by bmuselet         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = fdf
SRCS = main.c\
	   ft_reader.c\
	   ft_draw.c\
	   ft_atoi_fdf.c\
	   ft_check_error.c\
	   ft_keycode.c\

OBJS = $(SRCS:.c=.o)
INC = libft.h\
fdf.h\
CC = cc
FLAGS = -lmlx -framework OpenGl -framework AppKit -flto
LIB_PATH = libft/
LIB = libft/libft.a

.PHONY: all clean fclean re

all : $(NAME)

$(NAME) :
	@echo "\033[1;91mCompilation...\033[0m"
	@make re -C $(LIB_PATH)
	@$(CC) $(FLAGS) -c $(SRCS)
	@$(CC) $(FLAGS) -o $(NAME) $(OBJS) $(LIB)
	@echo "\033[1;91mCompilation complete !\033[0m" 

clean:
		@make clean -C $(LIB_PATH)
		@/bin/rm -f $(OBJS)
		@echo "\033[1;91m$(OBJS) removed !\033[0m"

fclean: clean
		@make fclean -C $(LIB_PATH)
		@/bin/rm -f $(NAME)
		@echo "\033[1;91m$(NAME) removed !\033[0m"

re: fclean all

