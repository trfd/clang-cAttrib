set(LLVM_LINK_COMPONENTS
  Support
  )

add_clang_unittest(ToolingTests
  CommentHandlerTest.cpp
  CompilationDatabaseTest.cpp
  ToolingTest.cpp
  RecursiveASTVisitorTest.cpp
  RefactoringTest.cpp
  RewriterTest.cpp
  RefactoringCallbacksTest.cpp
  ReplacementsYamlTest.cpp
  )

target_link_libraries(ToolingTests
  clangAST
  clangASTMatchers
  clangBasic
  clangFrontend
  clangLex
  clangRewrite
  clangTooling
  )
