
set(SRC
    src/ImplicitAgent.cpp
    src/ImplicitEngine.cpp
    src/lq2D.cpp
    src/Parser.cpp
)

set(INC
    src
    include
    include/proximitydatabase
    ../external
)

add_library(implicit_lib ${SRC})
target_include_directories(implicit_lib PUBLIC ${INC})
