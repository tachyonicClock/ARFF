enable_testing()

add_executable( 
    arffUnitTests
    arff_attr_t.cpp
    arff_instance_t.cpp
    arff_parser_t.cpp
    arff_token_t.cpp
    arff_value_t.cpp
    main.cpp
    arff_data_t.cpp
    arff_lexer_t.cpp
    arff_scanner_t.cpp
    arff_utils_t.cpp
)
file( COPY
    cases
    DESTINATION "${PROJECT_BINARY_DIR}/tests"
)
target_link_libraries(arffUnitTests 
    gtest
    gtest_main 
    ARFF
    pthread)
add_test(
    arffUnitTests
    arffUnitTests)