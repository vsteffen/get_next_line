# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: vsteffen <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2016/02/07 16:45:25 by vsteffen          #+#    #+#              #
#    Updated: 2016/02/07 16:45:29 by vsteffen         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libft.a

CC =	/usr/bin/clang
RM =	/bin/rm
MAKE =	/usr/bin/make
MKDIR =	/bin/mkdir
AR =	/usr/bin/ar
RANLIB = /usr/bin/ranlib

SRC = ft_atoi.c \
	  ft_bzero.c \
	  ft_isalnum.c \
	  ft_isalpha.c \
	  ft_isascii.c \
	  ft_isdigit.c \
	  ft_islower.c \
	  ft_isspace.c \
	  ft_isupper.c \
	  ft_isprint.c \
	  ft_itoa.c \
	  ft_lstadd.c \
	  ft_lstdel.c \
	  ft_lstdelone.c \
	  ft_lstpcontent.c \
	  ft_lstmap.c \
	  ft_lstnew.c \
	  ft_lstiter.c \
	  ft_memalloc.c \
	  ft_memccpy.c \
	  ft_memchr.c \
	  ft_memcmp.c \
	  ft_memcpy.c \
	  ft_memdel.c \
	  ft_memmove.c \
	  ft_memset.c \
	  ft_putchar.c \
	  ft_putchar_fd.c \
	  ft_putendl.c \
	  ft_putendl_fd.c \
	  ft_putnbr.c \
	  ft_putnbr_fd.c \
	  ft_putstr.c \
	  ft_putstr_fd.c \
	  ft_strcat.c \
	  ft_strchr.c \
	  ft_strclr.c \
	  ft_strcmp.c \
	  ft_strcpy.c \
	  ft_strdel.c \
	  ft_strdup.c \
	  ft_strequ.c \
	  ft_striter.c \
	  ft_striteri.c \
	  ft_strjoin.c \
	  ft_strlcat.c \
	  ft_strlen.c \
	  ft_strmap.c \
	  ft_strmapi.c \
	  ft_strncat.c \
	  ft_strncmp.c \
	  ft_strncpy.c \
	  ft_strnequ.c \
	  ft_strnew.c \
	  ft_strnstr.c \
	  ft_strrchr.c \
	  ft_strsplit.c \
	  ft_strstr.c \
	  ft_strsub.c \
	  ft_strtrim.c \
	  ft_tolower.c \
	  ft_toupper.c \
	  ft_clear.c \
	  ft_colors.c

OBJ = $(patsubst %.c, $(OPATH)/%.o, $(SRC))

CFLAGS = -Wall -Wextra -Werror -I $(HPATH)

ROOT =		$(shell /bin/pwd)
OPATH =		$(ROOT)/objs
CPATH =		$(ROOT)/srcs
HPATH =		$(ROOT)/includes

.PHONY: all clean fclean re

all: $(OPATH) $(NAME)

$(NAME): $(OBJ)
	@echo "Creating OBJ files"
	@echo "Building $@"
	@$(AR) rc $@ $(OBJ)
	@$(RANLIB) $@
	@echo "\033[34mAll is done!\033[0m"

$(OPATH)/%.o: $(CPATH)/%.c
	@$(CC) $(CFLAGS) -c $< -o $@

$(OPATH):
	@echo "Creating OBJ directory"
	@$(MKDIR) $@

clean:
	@echo "Deleting OBJS"
	@$(RM) -Rf $(OPATH)

fclean: clean
	@echo "Deleting $(NAME)"
	@$(RM) -f $(NAME)
	@echo "\033[34mAll clear!\033[0m"

re: fclean all
