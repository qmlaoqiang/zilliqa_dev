add_library(Utils AddressConversion.cpp BitVector.cpp DataConversion.cpp Logger.cpp SanityChecks.cpp Scheduler.cpp ShardSizeCalculator.cpp TimeUtils.cpp RandomGenerator.cpp RootComputation.cpp IPConverter.cpp UpgradeManager.cpp SWInfo.cpp FileSystem.cpp ScillaUtils.cpp MemoryStats.cpp CommonUtils.cpp)
target_include_directories(Utils PUBLIC ${PROJECT_SOURCE_DIR}/src Boost)
target_link_libraries(Utils INTERFACE Threads::Threads curl)
target_link_libraries(Utils PUBLIC g3logger CryptoUtils Constants MessageSWInfo )