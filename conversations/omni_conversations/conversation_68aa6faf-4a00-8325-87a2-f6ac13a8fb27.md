# Conversation 68aa6faf-4a00-8325-87a2-f6ac13a8fb27

**User [2025-08-23T19:49:49.522000]:**
I'm getting this error in blender 2.5 when trying to render: # Blender 4.5.1, Commit date: 2025-07-29 05:31, Hash b0a72b245dcf
Saved "testRenders-Bohemia-250823.blend"  # Info

# backtrace
Exception Record:

ExceptionCode         : EXCEPTION_ACCESS_VIOLATION
Exception Address     : 0x00007FF698DC72A0
Exception Module      : blender.exe
Exception Flags       : 0x00000000
Exception Parameters  : 0x2
	Parameters[0] : 0x0000000000000001
	Parameters[1] : 0x0000000000000000


Stack trace:
blender.exe         :0x00007FF698DC7200  blender::Array<blender::SimpleMapSlot<std::pair<int,int>,blender::meshintersect::ITT_value>,1,blend
blender.exe         :0x00007FF698DC6320  blender::Map<std::pair<int,int>,blender::meshintersect::ITT_value,0,blender::PythonProbingStrategy<
blender.exe         :0x00007FF698DC8020  blender::meshintersect::trimesh_nary_intersect
blender.exe         :0x00007FF698DCDC70  blender::meshintersect::boolean_trimesh
blender.exe         :0x00007FF698DCDA60  blender::meshintersect::boolean_mesh
blender.exe         :0x00007FF696D51CE0  blender::geometry::boolean::mesh_boolean_mesh_arr
blender.exe         :0x00007FF696D51410  blender::geometry::boolean::mesh_boolean
blender.exe         :0x00007FF696822540  non_float_boolean_mesh
blender.exe         :0x00007FF696821600  modify_mesh
blender.exe         :0x00007FF6960B8550  blender::bke::mesh_calc_modifiers
blender.exe         :0x00007FF6960B83D0  blender::bke::mesh_build_data
blender.exe         :0x00007FF6960B9470  blender::bke::mesh_data_update
blender.exe         :0x00007FF696005040  BKE_object_handle_data_update
blender.exe         :0x00007FF696004EE0  BKE_object_eval_uber_data
blender.exe         :0x00007FF6962C05E0  blender::deg::`anonymous namespace'::evaluate_node
blender.exe         :0x00007FF6962C0410  blender::deg::`anonymous namespace'::deg_task_run_func
blender.exe         :0x00007FF6961C1010  tbb::detail::d1::function_task<Task>::execute
tbb12.dll           :0x00007FFA52DB53A0  tbb::detail::r1::isolate_within_arena
tbb12.dll           :0x00007FFA52DB1CA0  tbb::detail::r1::is_tbbmalloc_used
tbb12.dll           :0x00007FFA52DCAD30  tbb::detail::r1::capture_fp_settings
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Threads:
Thread : 00000f54
ntdll.dll           :0x00007FFA7DB42F20  NtDelayExecution
ntdll.dll           :0x00007FFA7DABDAD0  RtlDelayExecution
KERNELBASE.dll      :0x00007FFA7B1D65E0  SleepEx
blender.exe         :0x00007FF69653CDB0  wm_window_events_process
blender.exe         :0x00007FF69652F330  WM_main
blender.exe         :0x00007FF695B3F870  main
blender.exe         :0x00007FF698C6AF14  __scrt_common_main_seh
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001584
ntdll.dll           :0x00007FFA7DB433F0  ZwWaitForMultipleObjects
KERNELBASE.dll      :0x00007FFA7B1ADE20  WaitForMultipleObjectsEx
KERNELBASE.dll      :0x00007FFA7B1ADE00  WaitForMultipleObjects
windhawk.dll        :0x00007FFA5B0DDCA0  GlobalHookSessionStart
windhawk.dll        :0x00007FFA5B0DDCA0  GlobalHookSessionStart
windhawk.dll        :0x00007FFA5B0DDCA0  GlobalHookSessionStart
windhawk.dll        :0x00007FFA5B0DDCA0  GlobalHookSessionStart
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000028f0
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000013b8
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000013f0
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000012c8
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00002840
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001514
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 0000479c
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001f9c
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001b80
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001acc
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001cd0
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001b5c
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001c24
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001028
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001adc
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001a60
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
IlmThread.dll       :0x00007FFA52AB49C0  IlmThread_3_3::Semaphore::wait
IlmThread.dll       :0x00007FFA52AB37A0  IlmThread_3_3::ThreadPool::setThreadProvider
IlmThread.dll       :0x00007FFA52AB1290  IlmThread_3_3::supportsThreads
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000016e0
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF695B963C0  delayed_close_thread_run
blender.exe         :0x00007FF695B94560  std::thread::_Invoke<std::tuple<void (__cdecl*)(void)>,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000015b8
ntdll.dll           :0x00007FFA7DB433F0  ZwWaitForMultipleObjects
KERNELBASE.dll      :0x00007FFA7B1ADE20  WaitForMultipleObjectsEx
KERNELBASE.dll      :0x00007FFA7B1ADE00  WaitForMultipleObjects
nvoglv64.dll        :0x00007FF9D56AC930  DrvPresentBuffers
nvoglv64.dll        :0x00007FF9D56AC930  DrvPresentBuffers
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000013d8
ntdll.dll           :0x00007FFA7DB433F0  ZwWaitForMultipleObjects
KERNELBASE.dll      :0x00007FFA7B1ADE20  WaitForMultipleObjectsEx
KERNELBASE.dll      :0x00007FFA7B1ADE00  WaitForMultipleObjects
nvoglv64.dll        :0x00007FF9D5A21950  vk_gr2608GetInstanceProcAddr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00004920
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
nvoglv64.dll        :0x00007FF9D567C2F0  DrvValidateVersion
nvoglv64.dll        :0x00007FF9D5A8BE30  vkGetInstanceProcAddr
nvoglv64.dll        :0x00007FF9D567C2F0  DrvValidateVersion
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000019c0
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
nvoglv64.dll        :0x00007FF9D567C2F0  DrvValidateVersion
nvoglv64.dll        :0x00007FF9D5A8BE30  vkGetInstanceProcAddr
nvoglv64.dll        :0x00007FF9D567C2F0  DrvValidateVersion
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001964
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
nvoglv64.dll        :0x00007FF9D567C2F0  DrvValidateVersion
nvoglv64.dll        :0x00007FF9D5A8BE30  vkGetInstanceProcAddr
nvoglv64.dll        :0x00007FF9D567C2F0  DrvValidateVersion
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001a00
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
nvoglv64.dll        :0x00007FF9D567C2F0  DrvValidateVersion
nvoglv64.dll        :0x00007FF9D5A8BE30  vkGetInstanceProcAddr
nvoglv64.dll        :0x00007FF9D567C2F0  DrvValidateVersion
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001c5c
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
nvoglv64.dll        :0x00007FF9D567C2F0  DrvValidateVersion
nvoglv64.dll        :0x00007FF9D5BE31C0  vk_icdNegotiateLoaderICDInterfaceVersion
nvoglv64.dll        :0x00007FF9D5BE31C0  vk_icdNegotiateLoaderICDInterfaceVersion
nvoglv64.dll        :0x00007FF9D567C2F0  DrvValidateVersion
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001500
win32u.dll          :0x00007FFA7B56ACB0  NtUserMsgWaitForMultipleObjectsEx
nvoglv64.dll        :0x00007FF9D567C2F0  DrvValidateVersion
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 0000156c
ntdll.dll           :0x00007FFA7DB46550  NtWaitForWorkViaWorkerFactory
ntdll.dll           :0x00007FFA7DA71C80  RtlAcquireSRWLockExclusive
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000015a0
ntdll.dll           :0x00007FFA7DB433F0  ZwWaitForMultipleObjects
KERNELBASE.dll      :0x00007FFA7B1ADE20  WaitForMultipleObjectsEx
combase.dll         :0x00007FFA7D69E130  RoParameterizedTypeExtraGetTypeSignature
combase.dll         :0x00007FFA7D69E130  RoParameterizedTypeExtraGetTypeSignature
combase.dll         :0x00007FFA7D69E130  RoParameterizedTypeExtraGetTypeSignature
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000019a0
win32u.dll          :0x00007FFA7B56ACB0  NtUserMsgWaitForMultipleObjectsEx
directmanipulation.dll:0x00007FFA4E313114  Symbols not available


Thread : 00001588
ntdll.dll           :0x00007FFA7DB433F0  ZwWaitForMultipleObjects
KERNELBASE.dll      :0x00007FFA7B1ADE20  WaitForMultipleObjectsEx
KERNELBASE.dll      :0x00007FFA7B1ADE00  WaitForMultipleObjects
blender.exe         :0x00007FF69658BA20  _ptw32_callUserDestroyRoutines
blender.exe         :0x00007FF6965906D0  sem_timedwait
blender.exe         :0x00007FF69658BA20  _ptw32_callUserDestroyRoutines
blender.exe         :0x00007FF69615F1B0  BLI_thread_queue_pop_timeout
blender.exe         :0x00007FF6964AB920  blender::gpu::VKDevice::submission_runner
blender.exe         :0x00007FF6961C0F70  TaskPool::background_task_run
blender.exe         :0x00007FF69658D810  _ptw32_threadStart
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001598
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001564
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 0000158c
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001594
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000017b0
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000016ac
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001664
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000017e4
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 0000497c
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 0000134c
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001a38
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001c08
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000018d0
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001ac0
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001af0
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00001c04
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
blender.exe         :0x00007FF6964A4A80  blender::gpu::GPUWorker::run
blender.exe         :0x00007FF6964A4100  std::thread::_Invoke<std::tuple<<lambda_220f905aeb1358f2e101a786c348f861> >,0>
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000023b0
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 0000238c
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00003260
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00002294
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000024fc
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00003e20
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00002568
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00002750
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000025dc
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000025e0
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00002608
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000025d8
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000027c0
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000027b8
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
tbb12.dll           :0x00007FFA52DC5070  tbb::detail::r1::set_end_of_input
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 0000389c
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000038a4
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000027fc
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00002850
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00002588
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 0000488c
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000028e8
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 000028cc
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00004eac
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00004e30
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00004eb4
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00004de8
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00004dec
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00004df0
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00004df4
ntdll.dll           :0x00007FFA7DB464F0  ZwWaitForAlertByThreadId
ntdll.dll           :0x00007FFA7DA89C80  RtlSleepConditionVariableSRW
KERNELBASE.dll      :0x00007FFA7B1ADBE0  SleepConditionVariableSRW
MSVCP140.dll        :0x00007FFA4C372820  std::_Winerror_message
MSVCP140.dll        :0x00007FFA4C372BB0  Cnd_wait
OpenImageIO_Util.dll:0x00007FFA40FFA020  OpenImageIO_v3_0::paropt::operator=
OpenImageIO_Util.dll:0x00007FFA40FF5EA0  OpenImageIO_v3_0::Sysutil::usleep
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00004df8
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
nvcuda64.dll        :0x00007FF9CA0D5A30  cuProfilerStop
nvcuda64.dll        :0x00007FF9CA030207  Symbols not available


Thread : 00000844
ntdll.dll           :0x00007FFA7DB42920  NtWaitForSingleObject
KERNELBASE.dll      :0x00007FFA7B1ACB10  WaitForSingleObjectEx
tbb12.dll           :0x00007FFA52DB1470  tbb::detail::r1::notify_by_address_all
tbb12.dll           :0x00007FFA52DC8390  tbb::detail::r1::current_context
tbb12.dll           :0x00007FFA52DC8390  tbb::detail::r1::current_context
tbb12.dll           :0x00007FFA52DC8390  tbb::detail::r1::current_context
tbb12.dll           :0x00007FFA52DC8390  tbb::detail::r1::current_context
blender.exe         :0x00007FF6961C13E0  tbb::detail::d1::task_group_base::wait
blender.exe         :0x00007FF6961C0E50  BLI_task_pool_work_and_wait
blender.exe         :0x00007FF6962C0480  blender::deg::`anonymous namespace'::evaluate_graph_threaded_stage
blender.exe         :0x00007FF6962C00F0  blender::deg::deg_evaluate_on_refresh
blender.exe         :0x00007FF6962A6F10  deg_flush_updates_and_refresh
blender.exe         :0x00007FF695DB7CC0  BKE_scene_graph_update_for_newframe_ex
blender.exe         :0x00007FF696515960  engine_render_view_layer
blender.exe         :0x00007FF696514D70  RE_engine_render
blender.exe         :0x00007FF69651E850  do_render_engine
blender.exe         :0x00007FF69651E090  do_render_compositor
blender.exe         :0x00007FF69651E8C0  do_render_full_pipeline
blender.exe         :0x00007FF69651BD00  RE_RenderFrame
blender.exe         :0x00007FF697279240  render_startjob
blender.exe         :0x00007FF696542800  do_job_thread
blender.exe         :0x00007FF69658D810  _ptw32_threadStart
ucrtbase.dll        :0x00007FFA7AF63660  wcsrchr
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Thread : 00002134
ntdll.dll           :0x00007FFA7DB46550  NtWaitForWorkViaWorkerFactory
ntdll.dll           :0x00007FFA7DA71C80  RtlAcquireSRWLockExclusive
KERNEL32.DLL        :0x00007FFA7CF8E8C0  BaseThreadInitThunk
ntdll.dll           :0x00007FFA7DA1C320  RtlUserThreadStart


Loaded Modules :
0x00007FF695870000 4.5.1.0              blender.exe C:\Program Files\Blender Foundation\Blender 4.5\blender.pdb 
0x00007FFA7D9E0000 10.0.26100.4768      ntdll.dll  
0x00007FFA7CF60000 10.0.26100.4768      KERNEL32.DLL  
0x00007FFA7B160000 10.0.26100.4946      KERNELBASE.dll  
0x00007FFA7C300000 10.0.26100.4946      USER32.dll  
0x00007FFA7B560000 10.0.26100.4946      win32u.dll  
0x00007FFA7D290000 10.0.26100.4768      GDI32.dll  
0x00007FFA7B630000 10.0.26100.4768      gdi32full.dll  
0x00007FFA7B0B0000 10.0.26100.4768      msvcp_win.dll  
0x00007FFA7AF60000 10.0.26100.4768      ucrtbase.dll  
0x00007FFA7B9A0000 10.0.26100.4652      ADVAPI32.dll  
0x00007FFA7D180000 7.0.26100.4768       msvcrt.dll  
0x00007FFA7CEB0000 10.0.26100.4768      sechost.dll  
0x00007FFA7D450000 10.0.26100.4768      RPCRT4.dll  
0x00007FFA7C730000 10.0.26100.4768      SHELL32.dll  
0x00007FFA7AC60000 10.0.26100.4768      wintypes.dll  
0x00007FFA7D570000 10.0.26100.4768      combase.dll  
0x00007FFA7C540000 10.0.26100.4768      ole32.dll  
0x00007FFA7C4D0000 10.0.26100.4768      SHLWAPI.dll  
0x00007FFA7B8B0000 10.0.26100.4768      OLEAUT32.dll  
0x00007FFA7B7B0000 10.0.26100.4946      shcore.dll  
0x00007FFA7B770000 10.0.26100.4484      IMM32.dll  
0x00007FFA5F900000 6.10.26100.4768      COMCTL32.dll  
0x00007FFA739E0000 10.0.26100.1150      VERSION.dll  
0x00007FFA70CB0000 10.0.26100.4202      dbghelp.dll  
0x00007FFA779F0000                      blender_cpu_check.dll  
0x00007FFA61AA0000 2021.13.0.0          tbbmalloc.dll  
0x00007FFA404B0000                      shaderc_shared.dll  
0x00007FFA52E10000                      Iex.dll  
0x00007FFA52DB0000 2021.13.0.0          tbb12.dll  
0x00007FFA52D00000 1.3.296.0            vulkan-1.dll  
0x00007FFA52C30000                      OpenEXR.dll  
0x00007FFA52BD0000                      Imath.dll  
0x00007FFA52B90000 1.39.2.0             MaterialXFormat.dll  
0x00007FFA4AC60000 1.39.2.0             MaterialXCore.dll  
0x00007FFA3E800000 4.4.0.0              embree4.dll  
0x00007FF9E8020000                      cycles_kernel_oneapi_aot.dll  
0x00007FFA3E370000                      OpenColorIO_2_4.dll  
0x00007FFA40F90000 3.0.6.0              OpenImageIO_Util.dll  
0x00007FFA3DC70000 3.0.6.0              OpenImageIO.dll  
0x00007FFA52B60000 2.3.3.0              OpenImageDenoise.dll  
0x00007FF9E6A80000                      oslcomp.dll  
0x00007FFA52B30000                      oslquery.dll  
0x00007FF9E1A10000                      oslexec.dll  
0x00007FFA3DA20000 61.7.100.0           avformat-61.dll  
0x00007FFA7D2C0000 10.0.26100.4768      WS2_32.dll  
0x00007FF9DE310000 61.19.101.0          avcodec-61.dll  
0x00007FF9DD220000 59.39.100.0          avutil-59.dll  
0x00007FFA73310000 61.3.100.0           avdevice-61.dll  
0x00007FF9E66C0000 8.0.0.0              sycl8.dll  
0x00007FFA4C950000 8.3.100.0            swscale-8.dll  
0x00007FFA402E0000 1.2.2.0              sndfile.dll  
0x00007FFA3D890000 1.23.1.0             OpenAL32.dll  
0x00007FFA2B990000 12.0.0.0             openvdb.dll  
0x00007FFA4B610000                      epoxy-0.dll  
0x00007FFA77EC0000 10.0.26100.4768      dxgi.dll  
0x00007FFA40E70000                      gmp-10.dll  
0x00007FFA4C360000 14.29.30139.0        MSVCP140.dll  
0x00007FFA52B00000 14.29.30139.0        MSVCP140_2.dll  
0x00007FFA7A7D0000 10.0.26100.4202      CFGMGR32.dll  
0x00007FFA52AE0000 14.29.30139.0        VCRUNTIME140.dll  
0x00007FFA75460000 14.29.30139.0        VCRUNTIME140_1.dll  
0x00007FFA78080000 10.0.26100.4768      dwmapi.dll  
0x00007FFA7AA00000 10.0.26100.4768      bcrypt.dll  
0x00007FFA52AD0000 2021.13.0.0          tbbmalloc_proxy.dll  
0x00007FF9DCBC0000 3.11.11150.1013      python311.dll  
0x00007FFA52AC0000                      libgmpxx.dll  
0x00007FFA52AB0000                      IlmThread.dll  
0x00007FF9E6480000                      OpenEXRCore.dll  
0x00007FF9D9EF0000 2.3.3.0              OpenImageDenoise_core.dll  
0x00007FFA77AE0000 10.0.26100.1         Secur32.dll  
0x00007FFA4B600000                      oslnoise.dll  
0x00007FFA4B420000 10.0.26100.1150      AVICAP32.dll  
0x00007FFA6B220000 10.0.26100.4202      WINMM.dll  
0x00007FFA4AC30000 10.0.26100.1150      MSVFW32.dll  
0x00007FFA79B40000 10.0.26100.4484      SSPICLI.DLL  
0x00007FF9D75D0000                      usd_ms.dll  
0x00007FF9F5360000 10.0.26100.4768      OPENGL32.dll  
0x00007FFA4AC00000 5.3.100.0            swresample-5.dll  
0x00007FFA4B410000 8.8.0.0              ur_win_proxy_loader.dll  
0x00007FFA3D660000 1.39.2.0             MaterialXRender.dll  
0x00007FFA4AB30000 1.39.2.0             MaterialXGenGlsl.dll  
0x00007FF9F5330000 10.0.26100.1150      GLU32.dll  
0x00007FFA4A810000 1.39.2.0             MaterialXGenMsl.dll  
0x00007FF9E63C0000 1.39.2.0             MaterialXGenShader.dll  
0x00007FFA78010000 10.0.26100.4768      dxcore.dll  
0x00007FF9E6300000 0.11.8.0             ur_loader.dll  
0x00007FFA77E30000 10.0.26100.4768      directxdatabasehelper.dll  
0x00007FFA79890000 10.0.26100.4768      kernel.appcore.dll  
0x00007FFA7B590000 10.0.26100.4768      bcryptPrimitives.dll  
0x00007FFA5B0C0000 1.6.1.0              windhawk.dll  
0x00007FFA5ACC0000                      dark-menus_1.3.1_243728.dll  
0x00007FFA77CE0000 10.0.26100.4768      UxTheme.dll  
0x00007FFA5AAC0000                      slick-window-arrangement_1.0.2_278571.dll  
0x00007FFA5AE30000                      libc++.whl  
0x00007FFA5B000000                      libunwind.whl  
0x00007FFA5AAA0000                      modernize-folder-picker-dialog_1.0.0_273224.dll  
0x00007FFA78730000 10.0.26100.4946      windows.storage.dll  
0x00007FFA7AA30000 10.0.26100.4768      profapi.dll  
0x00007FFA7A0E0000 10.0.26100.4768      CRYPTBASE.DLL  
0x00007FFA7C250000 2001.12.10941.16384  clbcatq.dll  
0x00007FFA72CC0000 10.0.26100.4768      MMDevApi.dll  
0x00007FFA7A780000 10.0.26100.1150      DEVOBJ.dll  
0x00007FFA63200000 10.0.26100.4768      AUDIOSES.DLL  
0x00007FFA78410000 10.0.26100.1150      resourcepolicyclient.dll  
0x00007FFA7A710000 10.0.26100.3912      powrprof.dll  
0x00007FFA7A530000 10.0.26100.1301      UMPDC.dll  
0x00007FFA6C740000 10.0.26100.4768      windows.staterepositorycore.dll  
0x00007FF9D4C80000 32.0.15.8097         nvoglv64.dll  
0x00007FFA77BA0000 10.0.26100.4768      WTSAPI32.dll  
0x00000230A6D80000 10.0.26100.4768      SETUPAPI.dll  
0x00007FFA7A150000 10.0.26100.4768      msasn1.dll  
0x00007FFA72960000 10.0.26100.3624      cryptnet.dll  
0x00007FFA7ADE0000 10.0.26100.4768      CRYPT32.dll  
0x00007FFA7A1C0000 10.0.26100.4768      wldp.dll  
0x00007FFA71830000 10.0.26100.4768      drvstore.dll  
0x00007FFA7ABD0000 10.0.26100.4768      WINTRUST.dll  
0x00007FFA799C0000 10.0.26100.4202      ntmarta.dll  
0x00007FFA7C700000 10.0.26100.4202      imagehlp.dll  
0x00007FFA7A0F0000 10.0.26100.4768      CRYPTSP.dll  
0x00007FFA797F0000 10.0.26100.4768      rsaenh.dll  
0x00007FFA6CAE0000 32.0.15.8097         nvgpucomp64.dll  
0x00007FFA5D4C0000 4.8.9032.0           rometadata.dll  
0x00007FFA7C0E0000 10.0.26100.4768      MSCTF.dll  
0x00007FFA75350000 7.0.26100.4768       PROPSYS.dll  
0x00007FFA629B0000 32.0.15.8097         nvapi64.dll  
0x00007FFA5D500000 10.0.26100.4768      DispBroker.dll  
0x00007FF9CDE40000 32.0.15.8097         nvrtum64.dll  
0x00007FF9E6250000 7.1.0.0              NvCameraAllowlisting64.dll  
0x00007FFA08550000 32.0.15.8097         nvppex.dll  
0x00007FFA7A230000 10.0.26100.4768      WINSTA.dll  
0x00007FFA4FAA0000 10.0.26100.4202      dataexchange.dll  
0x00007FFA6BBB0000 10.0.26100.4768      twinapi.appcore.dll  
0x00007FFA4AB00000 1.5.2.0              Wintab32.dll  
0x00007FFA4E530000 10.0.26100.4768      explorerframe.dll  
0x00007FFA4E2D0000 10.0.26100.4946      directmanipulation.dll  
0x00007FFA71520000 10.0.26100.4768      textinputframework.dll  
0x00007FFA77700000 10.0.26100.4202      CoreMessaging.dll  
0x00007FFA734C0000 10.0.26100.4768      CoreUIComponents.dll  
0x00007FFA5BB50000 7.2.26100.4768       Oleacc.dll  
0x00007FFA7D340000 10.0.26100.3624      coml2.dll  
0x00007FFA47A30000 10.0.26100.1         LINKINFO.dll  
0x00007FFA58040000 10.0.26100.4768      Windows.System.Launcher.dll  
0x00007FFA58C60000 10.0.26100.4768      Windows.StateRepositoryPS.dll  
0x00007FFA57E20000 10.0.26100.4768      Windows.FileExplorer.Common.dll  
0x00000230A92A0000 3.11.11150.1013      python3.DLL  
0x00007FFA4A000000 3.11.11150.1013      _socket.pyd  
0x00007FFA792F0000 10.0.26100.4768      IPHLPAPI.DLL  
0x00007FFA4B400000 3.11.11150.1013      select.pyd  
0x00007FF9E4350000                      _multiarray_umath.cp311-win_amd64.pyd  
0x00007FFA49FE0000                      _multiarray_tests.cp311-win_amd64.pyd  
0x00007FFA402B0000 3.11.11150.1013      _ctypes.pyd  
0x00007FFA4ABF0000                      libffi-8.dll  
0x00007FFA18700000                      _umath_linalg.cp311-win_amd64.pyd  
0x00007FFA3D870000                      _pocketfft_internal.cp311-win_amd64.pyd  
0x00007FFA288C0000                      mtrand.cp311-win_amd64.pyd  
0x00007FFA3D630000                      bit_generator.cp311-win_amd64.pyd  
0x00007FFA3D600000                      _common.cp311-win_amd64.pyd  
0x00007FFA49FD0000 3.11.11150.1013      _hashlib.pyd  
0x00007FF9CD900000 3.1.5.0              libcrypto-3.dll  
0x00007FFA28870000                      _bounded_integers.cp311-win_amd64.pyd  
0x00007FFA2B970000                      _mt19937.cp311-win_amd64.pyd  
0x00007FFA28850000                      _philox.cp311-win_amd64.pyd  
0x00007FFA28830000                      _pcg64.cp311-win_amd64.pyd  
0x00007FFA28810000                      _sfc64.cp311-win_amd64.pyd  
0x00007FFA1B420000                      _generator.cp311-win_amd64.pyd  
0x00007FFA287F0000 3.11.11150.1013      _bz2.pyd  
0x00007FFA287C0000 3.11.11150.1013      _lzma.pyd  
0x00007FFA28780000 3.11.11150.1013      pyexpat.pyd  
0x00007FFA402A0000 3.11.11150.1013      _uuid.pyd  
0x00007FFA1B3F0000 3.11.11150.1013      _elementtree.pyd  
0x00007FFA4E380000 10.0.26100.4768      ApplicationTargetedFeatureDatabase.dll  
0x00007FFA286A0000 3.11.11150.1013      _ssl.pyd  
0x00007FF9E6160000 3.1.5.0              libssl-3.dll  
0x00007FF9CC360000                      hiprt64.dll  
0x00007FF9CBF60000 32.0.15.8097         nvcuda.dll  
0x00007FF9C9E30000 32.0.15.8097         nvcuda64.dll  
0x00007FF9C9D90000                      nvdxgdmal64.dll  
0x00007FF9C99C0000 2.3.3.0              OpenImageDenoise_device_cuda.dll  
0x00007FF9C34D0000 9.0.2.0              nvoptix.dll  

# Python backtrace

Help me fix ittr

**System [2025-08-23T19:49:49.916488]:**


**Assistant [2025-08-23T19:49:50.813066]:**


**Tool [2025-08-23T19:50:09.662959]:**


**Tool [2025-08-23T19:50:26.491186]:**


**Tool [2025-08-23T19:50:34.234386]:**


**Tool [2025-08-23T19:50:37.604982]:**


**Tool [2025-08-23T19:50:52.230282]:**


**Tool [2025-08-23T19:51:07.760857]:**


**Tool [2025-08-23T19:51:11.701874]:**


**Tool [2025-08-23T19:51:15.064412]:**


**Tool [2025-08-23T19:51:21.076299]:**


**Assistant [2025-08-23T19:51:22.445328]:**
Diagnosis: you’re on Blender 4.5.1. The crash occurs inside the Boolean pipeline (`meshintersect::trimesh_nary_intersect → boolean_mesh → geometry::boolean`). Root cause is almost always invalid/non-manifold operands or an incompatible solver setting (the new Manifold solver only works on watertight, non-self-intersecting meshes). citeturn1search12turn8search8

Fix order:

1) Update first  
Install 4.5.2 LTS (bug-fix maintenance over 4.5.1). citeturn8search9

2) Hard-reset environment  
Launch Blender with factory prefs to exclude add-ons:  
`blender.exe --factory-startup`  
Open your .blend and render. Keep it factory until the issue is resolved. citeturn6search13

3) Isolate the offender fast  
Outliner → filter “Modifiers” → locate all objects with Boolean modifiers → toggle each modifier’s “Render” switch off → F12. Re-enable one by one until it crashes. The last toggled Boolean is the culprit.

4) Make operands valid geometry (on the culprit and its target)  
Object Mode: Ctrl-A → Apply All Transforms.  
Edit Mode:  
• Face Orientation: ensure all outward; flip as needed.  
• Mesh → Clean Up → Merge by Distance (tight threshold), Delete Loose, Degenerate Dissolve.  
• Select → Select All by Trait → Non-Manifold; repair holes/strays until selection is empty.  
• Mesh → Normals → Recalculate Outside; then Mesh → Normals → Clear Custom Split Normals Data.  
• Put a Triangulate modifier directly before the Boolean.

5) Use a compatible solver  
Boolean modifier: set Solver = **Exact** (or = **Manifold** only if both operands are truly manifold). Disable “Self” unless you explicitly need self-intersections. The Manifold solver requires watertight meshes; use Exact when in doubt. citeturn1search12

6) Modifier order hygiene  
Typical safe order on the operand meshes: Mirror → Solidify (if used) → **Triangulate** → **Boolean** → Subdivision. Avoid non-applied negative scales anywhere in the chain.

7) Batch-force safe settings (Text Editor → run once)

```python
import bpy

for o in bpy.data.objects:
    if o.type != 'MESH': 
        continue
    # force all Boolean modifiers to EXACT and push a Triangulate before them
    tri = None
    # ensure exactly one Triangulate at the front
    if not any(m.type == 'TRIANGULATE' for m in o.modifiers):
        tri = o.modifiers.new(name="TriangulatePreBoolean", type='TRIANGULATE')
        o.modifiers.move(len(o.modifiers)-1, 0)
    for m in o.modifiers:
        if m.type == 'BOOLEAN':
            try:
                m.solver = 'EXACT'   # Alternatives: 'FLOAT' (old Fast), 'MANIFOLD' (requires manifold)
            except Exception:
                pass
```

The available boolean solver enums (Exact / Float / Manifold) are defined in 4.5’s API; Manifold is only appropriate for manifold inputs. citeturn5search11

8) Geometry Nodes parity  
If you’re booleans-via-GN, set the Boolean node’s solver to **Exact** or ensure truly manifold inputs before using **Manifold**. Same constraints apply. citeturn5search11

9) Backend fallback (if renders still crash after geometry fixes)  
Vulkan is the default graphics backend in 4.5. If you suspect a driver/backend interaction, switch the backend to OpenGL in Preferences and retest renders. Revert to Vulkan once stable. citeturn4search7

10) External process hooks  
Your crash log shows `windhawk.dll` and other injected DLLs. Exclude `blender.exe` from Windhawk/global hooks to remove unknown code paths during render. Keep Blender on factory prefs during testing. citeturn6search13

This sequence resolves Boolean-path EXCEPTION_ACCESS_VIOLATIONs in 4.5.x by correcting operands, enforcing a safe solver, and removing environmental variables.

**System [Unknown Time]:**


**System [Unknown Time]:**


**System [Unknown Time]:**

