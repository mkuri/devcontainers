FROM mkuri/archlinux-base:latest

# Install main packages for c++ development
RUN pacman -Syu --noconfirm gcc gdb clang llvm lldb cmake cppcheck valgrind \
    && rm -rf /var/cache/pacman/pkg/*
    
# Install lib packages for c++ development
RUN pacman -Syu --noconfirm boost benchmark \
    && rm -rf /var/cache/pacman/pkg/*