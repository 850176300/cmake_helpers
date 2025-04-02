# This file is part of Desktop App Toolkit,
# a set of libraries for developing nice desktop applications.
#
# For license and copyright information please follow this link:
# https://github.com/desktop-app/legal/blob/master/LEGAL

add_library(nim_sdk_wrapper STATIC)
init_target(nim_sdk_wrapper "(external)")
add_library(desktop-app::nim_sdk_wrapper ALIAS nim_sdk_wrapper)

nice_target_sources(nim_sdk_wrapper ${libs_loc}/nim_sdk/wrapper/nim_cpp_wrapper
PRIVATE
    api/nim_cpp_global.cpp
    api/nim_cpp_global.h
    api/nim_cpp_msglog.cpp
    api/nim_cpp_msglog.h
    api/nim_cpp_nos.cpp
    api/nim_cpp_nos.h
    api/nim_cpp_pass_through_proxy.cpp
    api/nim_cpp_pass_through_proxy.h
    api/nim_cpp_plugin_in.cpp
    api/nim_cpp_plugin_in.h
    api/nim_cpp_robot.cpp
    api/nim_cpp_robot.h
    api/nim_cpp_rts.cpp
    api/nim_cpp_rts.h
    api/nim_cpp_session.cpp
    api/nim_cpp_session.h
    api/nim_cpp_session_online_service.cpp
    api/nim_cpp_session_online_service.h
    api/nim_cpp_signaling.cpp
    api/nim_cpp_signaling.h
    api/nim_cpp_subscribe_event.cpp
    api/nim_cpp_subscribe_event.h
    api/nim_cpp_super_team.cpp
    api/nim_cpp_super_team.h
    api/nim_cpp_sysmsg.cpp
    api/nim_cpp_sysmsg.h
    api/nim_cpp_talk.cpp
    api/nim_cpp_talk.h
    api/nim_cpp_talkex.h
    api/nim_cpp_talkex_collect.cpp
    api/nim_cpp_talkex_pin_message.cpp
    api/nim_cpp_talkex_quick_comment.cpp
    api/nim_cpp_team.cpp
    api/nim_cpp_team.h
    api/nim_cpp_tool.cpp
    api/nim_cpp_tool.h
    api/nim_cpp_user.cpp
    api/nim_cpp_user.h
    api/nim_cpp_vchat.cpp
    api/nim_cpp_vchat.h
    api/nim_cpp_ai.cpp
    api/nim_cpp_ai.h
    api/nim_cpp_client.cpp
    api/nim_cpp_client.h
    api/nim_cpp_data_sync.cpp
    api/nim_cpp_data_sync.h
    api/nim_cpp_doc_trans.cpp
    api/nim_cpp_doc_trans.h
    api/nim_cpp_friend.cpp
    api/nim_cpp_friend.h
    helper/nim_msglog_helper.h
    helper/nim_nos_helper.cpp
    helper/nim_nos_helper.h
    helper/nim_pass_through_proxy_helper.h
    helper/nim_robot_helper.cpp
    helper/nim_robot_helper.h
    helper/nim_sdk_loader_helper.cpp
    helper/nim_sdk_loader_helper.h
    helper/nim_session_helper.cpp
    helper/nim_session_helper.h
    helper/nim_session_online_service_helper.cpp
    helper/nim_session_online_service_helper.h
    helper/nim_signaling_helper.cpp
    helper/nim_signaling_helper.h
    helper/nim_subscribe_event_helper.cpp
    helper/nim_subscribe_event_helper.h
    helper/nim_super_team_helper.cpp
    helper/nim_super_team_helper.h
    helper/nim_sysmsg_helper.cpp
    helper/nim_sysmsg_helper.h
    helper/nim_talk_helper.cpp
    helper/nim_talk_helper.h
    helper/nim_talkex_helper_collect.cpp
    helper/nim_talkex_helper_collect.h
    helper/nim_talkex_helper_pin_message.cpp
    helper/nim_talkex_helper_pin_message.h
    helper/nim_talkex_helper_quick_comment.cpp
    helper/nim_talkex_helper_quick_comment.h
    helper/nim_team_helper.cpp
    helper/nim_team_helper.h
    helper/nim_tool_helper.h
    helper/nim_user_helper.cpp
    helper/nim_user_helper.h
    helper/nim_ai_helper.cpp
    helper/nim_ai_helper.h
    helper/nim_client_helper.cpp
    helper/nim_client_helper.h
    helper/nim_doc_trans_helper.cpp
    helper/nim_doc_trans_helper.h
    helper/nim_friend_helper.cpp
    helper/nim_friend_helper.h
    helper/nim_msg_helper.cpp
    helper/nim_msg_helper.h
    helper/nim_msglog_helper.cpp
    nim_sdk_cpp_wrapper.h
    nim_cpp_api.h
)

validate_d3d_compiler(nim_sdk_wrapper)

target_link_libraries(nim_sdk_wrapper
PUBLIC
    desktop-app::external_nim_sdk
)
