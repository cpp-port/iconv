cmake_minimum_required(VERSION 3.16)
project(iconv C)


list(APPEND library_source
include/iconv.h
libcharset/include/localcharset.h
lib/aliases.h
lib/aliases2.h
lib/aliases_aix.h
lib/aliases_aix_sysaix.h
lib/aliases_dos.h
lib/aliases_extra.h
lib/aliases_osf1.h
lib/aliases_osf1_sysosf1.h
lib/aliases_sysaix.h
lib/aliases_syshpux.h
lib/aliases_sysosf1.h
lib/aliases_syssolaris.h
lib/armscii_8.h
lib/ascii.h
lib/atarist.h
lib/big5.h
lib/big5hkscs1999.h
lib/big5hkscs2001.h
lib/big5hkscs2004.h
lib/big5hkscs2008.h
lib/big5_2003.h
lib/c99.h
lib/canonical.h
lib/canonical_aix.h
lib/canonical_aix_sysaix.h
lib/canonical_dos.h
lib/canonical_extra.h
lib/canonical_local.h
lib/canonical_local_sysaix.h
lib/canonical_local_syshpux.h
lib/canonical_local_sysosf1.h
lib/canonical_local_syssolaris.h
lib/canonical_osf1.h
lib/canonical_osf1_sysosf1.h
lib/canonical_sysaix.h
lib/canonical_syshpux.h
lib/canonical_sysosf1.h
lib/canonical_syssolaris.h
lib/ces_big5.h
lib/ces_gbk.h
lib/cjk_variants.h
lib/cns11643.h
lib/cns11643_1.h
lib/cns11643_15.h
lib/cns11643_2.h
lib/cns11643_3.h
lib/cns11643_4.h
lib/cns11643_4a.h
lib/cns11643_4b.h
lib/cns11643_5.h
lib/cns11643_6.h
lib/cns11643_7.h
lib/cns11643_inv.h
lib/converters.h
lib/cp1046.h
lib/cp1124.h
lib/cp1125.h
lib/cp1129.h
lib/cp1131.h
lib/cp1133.h
lib/cp1161.h
lib/cp1162.h
lib/cp1163.h
lib/cp1250.h
lib/cp1251.h
lib/cp1252.h
lib/cp1253.h
lib/cp1254.h
lib/cp1255.h
lib/cp1256.h
lib/cp1257.h
lib/cp1258.h
lib/cp437.h
lib/cp737.h
lib/cp775.h
lib/cp850.h
lib/cp852.h
lib/cp853.h
lib/cp855.h
lib/cp856.h
lib/cp857.h
lib/cp858.h
lib/cp860.h
lib/cp861.h
lib/cp862.h
lib/cp863.h
lib/cp864.h
lib/cp865.h
lib/cp866.h
lib/cp869.h
lib/cp874.h
lib/cp922.h
lib/cp932.h
lib/cp932ext.h
lib/cp936.h
lib/cp936ext.h
lib/cp943.h
lib/cp949.h
lib/cp950.h
lib/cp950ext.h
lib/dec_hanyu.h
lib/dec_kanji.h
lib/euc_cn.h
lib/euc_jisx0213.h
lib/euc_jp.h
lib/euc_kr.h
lib/euc_tw.h
lib/flags.h
lib/flushwc.h
lib/gb12345.h
lib/gb12345ext.h
lib/gb18030.h
lib/gb18030ext.h
lib/gb18030uni.h
lib/gb2312.h
lib/gbk.h
lib/gbkext1.h
lib/gbkext2.h
lib/gbkext_inv.h
lib/georgian_academy.h
lib/georgian_ps.h
lib/gunibreak.h
lib/gunicomp.h
lib/gunidecomp.h
lib/hkscs1999.h
lib/hkscs2001.h
lib/hkscs2004.h
lib/hkscs2008.h
lib/hp_roman8.h
lib/hz.h
lib/iconv_open1.h
lib/iconv_open2.h
lib/idn-free.h
lib/idna.h
lib/iso2022_cn.h
lib/iso2022_cnext.h
lib/iso2022_jp.h
lib/iso2022_jp1.h
lib/iso2022_jp2.h
lib/iso2022_jp3.h
lib/iso2022_kr.h
lib/iso646_cn.h
lib/iso646_jp.h
lib/iso8859_1.h
lib/iso8859_10.h
lib/iso8859_11.h
lib/iso8859_13.h
lib/iso8859_14.h
lib/iso8859_15.h
lib/iso8859_16.h
lib/iso8859_2.h
lib/iso8859_3.h
lib/iso8859_4.h
lib/iso8859_5.h
lib/iso8859_6.h
lib/iso8859_7.h
lib/iso8859_8.h
lib/iso8859_9.h
lib/isoir165.h
lib/isoir165ext.h
lib/java.h
lib/jisx0201.h
lib/jisx0208.h
lib/jisx0212.h
lib/jisx0213.h
lib/johab.h
lib/johab_hangul.h
lib/koi8_r.h
lib/koi8_ru.h
lib/koi8_t.h
lib/koi8_u.h
lib/ksc5601.h
lib/loops.h
lib/loop_unicode.h
lib/loop_wchar.h
lib/mac_arabic.h
lib/mac_centraleurope.h
lib/mac_croatian.h
lib/mac_cyrillic.h
lib/mac_greek.h
lib/mac_hebrew.h
lib/mac_iceland.h
lib/mac_roman.h
lib/mac_romania.h
lib/mac_thai.h
lib/mac_turkish.h
lib/mac_ukraine.h
lib/mulelao.h
lib/nextstep.h
lib/pr29.h
lib/pt154.h
lib/punycode.h
lib/relocatable.h
lib/riscos1.h
lib/rk1048.h
lib/shift_jisx0213.h
lib/sjis.h
lib/stringprep.h
lib/tcvn.h
lib/tds565.h
lib/tis620.h
lib/tld.h
lib/translit.h
lib/ucs2.h
lib/ucs2be.h
lib/ucs2internal.h
lib/ucs2le.h
lib/ucs2swapped.h
lib/ucs4.h
lib/ucs4be.h
lib/ucs4internal.h
lib/ucs4le.h
lib/ucs4swapped.h
lib/uhc_1.h
lib/uhc_2.h
lib/utf16.h
lib/utf16be.h
lib/utf16le.h
lib/utf32.h
lib/utf32be.h
lib/utf32le.h
lib/utf7.h
lib/utf8.h
lib/vietcomb.h
lib/viscii.h
libcharset/lib/localcharset.c
lib/iconv.c
lib/relocatable.c

)


add_library(${PROJECT_NAME} SHARED ${library_source})
add_library(static_${PROJECT_NAME} STATIC ${library_source})


if (MSVC)
    message(STATUS "${PROJECT_NAME} MSVC")
    target_compile_options(${PROJECT_NAME} PRIVATE "/MD$<$<CONFIG:Debug>:d>")
    target_link_options(${PROJECT_NAME} PRIVATE "/DEFAULTLIB:msvcrt$<$<CONFIG:Debug>:d>")
    target_link_options(${PROJECT_NAME} PRIVATE "/SUBSYSTEM:WINDOWS")
    target_link_options(${PROJECT_NAME} PRIVATE "/DEF:${CMAKE_CURRENT_SOURCE_DIR}/${PROJECT_NAME}.def")
    target_link_options(${PROJECT_NAME} PRIVATE "/IMPLIB:${LIBRARY_OUTPUT_PATH}/${PROJECT_NAME}.lib")
    target_link_libraries(${PROJECT_NAME} PRIVATE ${library_references} ${global_library_references})

elseif (${LINUX} OR ${__BSD__} OR ${ANDROID})



    #target_compile_options(${PROJECT_NAME} PRIVATE $<$<COMPILE_LANGUAGE:CXX>:-fpermissive  ${EXTRA_CXX_TARGET_COMPILER_OPTIONS}>)
    #target_compile_options(static_${PROJECT_NAME} PRIVATE $<$<COMPILE_LANGUAGE:CXX>:-fpermissive  ${EXTRA_CXX_TARGET_COMPILER_OPTIONS}>)
    target_compile_definitions(static_${PROJECT_NAME} PRIVATE CUBE)

    #if(${SUSE} OR ${OPENBSD})
    if(${OPENBSD} OR ${NETBSD})

        target_link_libraries(${PROJECT_NAME} PRIVATE iconv ${library_references} ${global_library_references})
        target_link_libraries(static_${PROJECT_NAME} PRIVATE ${static_library_references})

    else()


        #        pkg_check_modules(PKGCONFIG iconv)
        #        target_compile_options(${PROJECT_NAME} PRIVATE ${${PROJECT_NAME}_PKGCONFIG_CFLAGS})
        #        target_compile_options(static_${PROJECT_NAME} PRIVATE ${${PROJECT_NAME}_PKGCONFIG_CFLAGS})
        #        target_link_options(${PROJECT_NAME} PRIVATE ${${PROJECT_NAME}_PKGCONFIG_LDFLAGS})
        #        target_link_libraries(${PROJECT_NAME} PRIVATE ${library_references} ${global_library_references} ${${PROJECT_NAME}_PKGCONFIG_LIBRARIES})
        #        target_link_libraries(static_${PROJECT_NAME} PRIVATE ${static_library_references} ${${PROJECT_NAME}_PKGCONFIG_LIBRARIES})


        target_link_libraries(${PROJECT_NAME} PRIVATE ${library_references} ${global_library_references})
        target_link_libraries(static_${PROJECT_NAME} PRIVATE ${static_library_references})


    endif()

    target_link_options(${PROJECT_NAME} PRIVATE -Wl,-z,defs)
    # target_link_options(static_${PROJECT_NAME} PRIVATE --whole-archive)


endif()


list(APPEND library_include_directories ${CMAKE_CURRENT_SOURCE_DIR}/libcharset/include)
list(APPEND library_include_directories ${CMAKE_CURRENT_SOURCE_DIR}/../..)
list(APPEND library_include_directories ${CMAKE_CURRENT_SOURCE_DIR}/..)
list(APPEND library_include_directories ${CMAKE_CURRENT_SOURCE_DIR})
list(APPEND library_include_directories ${CMAKE_CURRENT_SOURCE_DIR}/../../../operating_system/operating_system-${PLATFORM_NAME}/configuration/${PROJECT_NAME})


target_include_directories(${PROJECT_NAME} PRIVATE ${library_include_directories})
target_include_directories(static_${PROJECT_NAME} PRIVATE ${library_include_directories})

