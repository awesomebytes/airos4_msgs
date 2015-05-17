cmake_minimum_required(VERSION 2.8.3)
project(airos4_msgs)

find_package(catkin REQUIRED
  COMPONENTS
    message_generation
    std_msgs
)


add_message_files(
  DIRECTORY msg
  FILES
    Accelerometer.msg
    Battery.msg
    Touch.msg
)

add_service_files(
  DIRECTORY srv
  FILES
    CheckGrammar.srv
    GetBool.srv
    GetFloat.srv
    GetHeartColor.srv
    GetListAudio.srv
    GetList.srv
    GetMouth.srv
    GetServoPos.srv
    GetString.srv
    HeartBeat.srv
    HeartFlashColor.srv
    MouthDrawImageFile.srv
    MouthDraw.srv
    MouthPrint.srv
    MoveBotmobile.srv
    MoveService.srv
    MoveServoRelative.srv
    MoveServo.srv
    Perform.srv
    PlayRandom.srv
    Play.srv
    Say.srv
    SetBool.srv
    SetColor.srv
    SetFloat.srv
    SetPerformance.srv
    SetString.srv
    StopAll.srv
    Stop.srv
    StringBool.srv
)

generate_messages(DEPENDENCIES std_msgs)

catkin_package(CATKIN_DEPENDS message_runtime)