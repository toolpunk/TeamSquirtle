# In this CMakeLists.txt we define which files
# are used to compile the application
set(kde4teamsquirtle_SRCS
   #application.cpp
   main.cpp
 )

# Set the name of the application
add_executable(kde4teamsquirtle ${kde4teamsquirtle_SRCS})

# Select which libraries we need to link to
target_link_libraries(kde4teamsquirtle Qt5::Widgets KF5::CoreAddons KF5::ConfigCore)

# Tell cmake to install the application binary
install(TARGETS kde4teamsquirtle DESTINATION ${LIB_INSTALL_DIR}/kconf_update_bin/)
install(FILES kde4teamsquirtle.upd DESTINATION ${KCONF_UPDATE_INSTALL_DIR})

# Install the color scheme

