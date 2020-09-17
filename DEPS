# This file is automatically processed to create .DEPS.git which is the file
# that gclient uses under git.
#
# See http://code.google.com/p/chromium/wiki/UsingGit
#
# To test manually, run:
#   python tools/deps2git/deps2git.py -o .DEPS.git -w <gclientdir>
# where <gcliendir> is the absolute path to the directory containing the
# .gclient file (the parent of 'src').
#
# Then commit .DEPS.git locally (gclient doesn't like dirty trees) and run
#   gclient sync..
# Verify the thing happened you wanted. Then revert your .DEPS.git change
# DO NOT CHECK IN CHANGES TO .DEPS.git upstream. It will be automatically
# updated by a bot when you modify this one.
#
# When adding a new dependency, please update the top-level .gitignore file
# to list the dependency's destination directory.

vars = {
  'chromium_git': 'https://chromium.googlesource.com',
  'swiftshader_git': 'https://swiftshader.googlesource.com',
  'dart_git': 'https://dart.googlesource.com',
  'fuchsia_git': 'https://fuchsia.googlesource.com',
  'github_git': 'https://github.com',
  'skia_git': 'https://skia.googlesource.com',
  # OCMock is for testing only so there is no google clone
  'ocmock_git': 'https://github.com/erikdoe/ocmock.git',
  'skia_revision': 'bf66ffbbd4ce79bc423fe469a2f90acebd3dba91',

  # When updating the Dart revision, ensure that all entries that are
  # dependencies of Dart are also updated to match the entries in the
  # Dart SDK's DEPS file for that revision of Dart. The DEPS file for
  # Dart is: https://github.com/dart-lang/sdk/blob/master/DEPS.
  # You can use //tools/dart/create_updated_flutter_deps.py to produce
  # updated revision list of existing dependencies.
  'dart_revision': 'eb24e3324908a0987881a05d64c7e8d45ead9c4a',

  # WARNING: DO NOT EDIT MANUALLY
  # The lines between blank lines above and below are generated by a script. See create_updated_flutter_deps.py
  'dart_args_tag': '1.6.0',
  'dart_boringssl_gen_rev': '429ccb1877f7987a6f3988228bc2440e61293499',
  'dart_boringssl_rev': '4dfd5af70191b068aebe567b8e29ce108cee85ce',
  'dart_collection_rev': '583693680fc067e34ca5b72503df25e8b80579f9',
  'dart_dart_style_tag': '1.3.7',
  'dart_http_retry_tag': '0.1.1',
  'dart_http_throttle_tag': '1.0.2',
  'dart_intl_tag': '0.16.1',
  'dart_linter_tag': '0.1.118',
  'dart_oauth2_tag': '1.6.0',
  'dart_protobuf_rev': '3746c8fd3f2b0147623a8e3db89c3ff4330de760',
  'dart_pub_rev': '04e237f78b2302d7f20d0b362554425e8deb8add',
  'dart_pub_semver_tag': 'v1.4.4',
  'dart_quiver-dart_tag': '246e754fe45cecb6aa5f3f13b4ed61037ff0d784',
  'dart_resource_rev': 'f8e37558a1c4f54550aa463b88a6a831e3e33cd6',
  'dart_root_certificates_rev': '7e5ec82c99677a2e5b95ce296c4d68b0d3378ed8',
  'dart_shelf_packages_handler_tag': '2.0.0',
  'dart_shelf_proxy_tag': '0.1.0+7',
  'dart_shelf_static_rev': 'v0.2.8',
  'dart_shelf_web_socket_tag': '0.2.2+3',
  'dart_sse_tag': 'e5cf68975e8e87171a3dc297577aa073454a91dc',
  'dart_stack_trace_tag': 'd3813ca0a77348e0faf0d6af0cc17913e36afa39',
  'dart_stagehand_tag': 'v3.3.9',
  'dart_stream_channel_tag': 'c446774fd077c9bdbd6235a7aadc661ef60a9727',
  'dart_test_reflective_loader_tag': '0.1.9',
  'dart_tflite_native_rev': '3c777c40608a2a9f1427bfe0028ab48e7116b4c1',
  'dart_typed_data_tag': 'f94fc57b8e8c0e4fe4ff6cfd8290b94af52d3719',
  'dart_usage_tag': '3.4.0',
  'dart_watcher_rev': 'fc3c9aae5d31d707b3013b42634dde8d8a1161b4',

  'ocmock_tag': 'v3.7.1',

  # Build bot tooling for iOS
  'ios_tools_revision': '69b7c1b160e7107a6a98d948363772dc9caea46f',

  # Checkout Android dependencies only on platforms where we build for Android targets.
  'download_android_deps': 'host_os == "mac" or host_os == "linux"',

  # Checkout Windows dependencies only if we are building on Windows.
  'download_windows_deps' : 'host_os == "win"',

  # Checkout Linux dependencies only when building on Linux.
  'download_linux_deps': 'host_os == "linux"',

  # An LLVM backend needs LLVM binaries and headers. To avoid build time
  # increases we can use prebuilts. We don't want to download this on every
  # CQ/CI bot nor do we want the average Dart developer to incur that cost.
  # So by default we will not download prebuilts. This varible is needed in
  # the flutter engine to ensure that Dart gn has access to it as well.
  "checkout_llvm": False,
}

gclient_gn_args_file = 'src/third_party/dart/build/config/gclient_args.gni'
gclient_gn_args = [
  'checkout_llvm'
]

# Only these hosts are allowed for dependencies in this DEPS file.
# If you need to add a new host, contact chrome infrastructure team.
allowed_hosts = [
  'chromium.googlesource.com',
  'fuchsia.googlesource.com',
  'github.com',
  'skia.googlesource.com',
]

deps = {
  'src': 'https://github.com/flutter/buildroot.git' + '@' + 'f83d1d75216e97fb696434bca1cb9a4e7a570fb6',

   # Fuchsia compatibility
   #
   # The dependencies in this section should match the layout in the Fuchsia gn
   # build. Eventually, we'll manage these dependencies together with Fuchsia
   # and not have to specific specific hashes.

  'src/third_party/benchmark':
   Var('fuchsia_git') + '/third_party/benchmark' + '@' + 'a779ffce872b4c811beef482e18bd0b63626aa42',

  'src/third_party/googletest':
   Var('fuchsia_git') + '/third_party/googletest' + '@' + '3fef9015bfe7617d57806cd7c73a653b28559fae',

  'src/third_party/rapidjson':
   Var('fuchsia_git') + '/third_party/rapidjson' + '@' + 'ef3564c5c8824989393b87df25355baf35ff544b',

  'src/third_party/harfbuzz':
   Var('fuchsia_git') + '/third_party/harfbuzz' + '@' + '9c55f4cf3313d68d68f68419e7a57fb0771fcf49',

  'src/third_party/libcxx':
   Var('fuchsia_git') + '/third_party/libcxx' + '@' + '7524ef50093a376f334a62a7e5cebf5d238d4c99',

  'src/third_party/libcxxabi':
   Var('fuchsia_git') + '/third_party/libcxxabi' + '@' + '74d1e602c76350f0760bf6907910e4f3a4fccffe',

  'src/third_party/glfw':
   Var('fuchsia_git') + '/third_party/glfw' + '@' + '999f3556fdd80983b10051746264489f2cb1ef16',

   # Chromium-style
   #
   # As part of integrating with Fuchsia, we should eventually remove all these
   # Chromium-style dependencies.

  'src/ios_tools':
   Var('chromium_git') + '/chromium/src/ios.git' + '@' + Var('ios_tools_revision'),

  'src/third_party/icu':
   Var('chromium_git') + '/chromium/deps/icu.git' + '@' + '8d29692df640668ed7e4d1817715440c4e05697a',

  'src/third_party/khronos':
   Var('chromium_git') + '/chromium/src/third_party/khronos.git' + '@' + '7122230e90547962e0f0c627f62eeed3c701f275',

  'src/third_party/boringssl':
   Var('github_git') + '/dart-lang/boringssl_gen.git' + '@' + Var('dart_boringssl_gen_rev'),

  'src/third_party/boringssl/src':
   'https://boringssl.googlesource.com/boringssl.git' + '@' + Var('dart_boringssl_rev'),

  'src/third_party/dart':
   Var('dart_git') + '/sdk.git' + '@' + Var('dart_revision'),

  # WARNING: Unused Dart dependencies in the list below till "WARNING:" marker are removed automatically - see create_updated_flutter_deps.py.

  'src/third_party/dart/third_party/pkg/args':
   Var('dart_git') + '/args.git' + '@' + Var('dart_args_tag'),

  'src/third_party/dart/third_party/pkg/async':
   Var('dart_git') + '/async.git@128c461a97dbdbd9336ba000ba5a5c02e79b8651',

  'src/third_party/dart/third_party/pkg/bazel_worker':
   Var('dart_git') + '/bazel_worker.git@26680d5e249b249c7216ab2fed0ac8ed4ee285c5',

  'src/third_party/dart/third_party/pkg/boolean_selector':
   Var('dart_git') + '/boolean_selector.git@665e6921ab246569420376f827bff4585dff0b14',

  'src/third_party/dart/third_party/pkg/charcode':
   Var('dart_git') + '/charcode.git@4a685faba42d86ebd9d661eadd1e79d0a1c34c43',

  'src/third_party/dart/third_party/pkg/cli_util':
   Var('dart_git') + '/cli_util.git@0.2.0',

  'src/third_party/dart/third_party/pkg/collection':
   Var('dart_git') + '/collection.git' + '@' + Var('dart_collection_rev'),

  'src/third_party/dart/third_party/pkg/convert':
   Var('dart_git') + '/convert.git@c1b01f832835d3d8a06b0b246a361c0eaab35d3c',

  'src/third_party/dart/third_party/pkg/crypto':
   Var('dart_git') + '/crypto.git@f7c48b334b1386bc5ab0f706fbcd6df8496a87fc',

  'src/third_party/dart/third_party/pkg/csslib':
   Var('dart_git') + '/csslib.git@681a6603f86bbbe64e8af42d722aef63b028d241',

  'src/third_party/dart/third_party/pkg/dart2js_info':
   Var('dart_git') + '/dart2js_info.git@0632a623b08e1f601c7eba99e0186a581ae799e9',

  'src/third_party/dart/third_party/pkg/dartdoc':
   Var('dart_git') + '/dartdoc.git@2bef0f260594b822f55c8c8f777d9c4c1ea8f76c',

  'src/third_party/dart/third_party/pkg/ffi':
   Var('dart_git') + '/ffi.git@454ab0f9ea6bd06942a983238d8a6818b1357edb',

  'src/third_party/dart/third_party/pkg/fixnum':
   Var('dart_git') + '/fixnum.git@16d3890c6dc82ca629659da1934e412292508bba',

  'src/third_party/dart/third_party/pkg/glob':
   Var('dart_git') + '/glob.git@e9f4e6b7ae8abe5071461cf8f47191bb19cf7ef6',

  'src/third_party/dart/third_party/pkg/html':
   Var('dart_git') + '/html.git@083a36cd801a4b787ba156b7c6e4c8b2e2daed4a',

  'src/third_party/dart/third_party/pkg/http':
   Var('dart_git') + '/http.git@7b55a2c62a5f6fb680ad7a4607bab7281a235563',

  'src/third_party/dart/third_party/pkg/http_multi_server':
   Var('dart_git') + '/http_multi_server.git@ea269f79321d659208402088f3297e8920a88ee6',

  'src/third_party/dart/third_party/pkg/http_parser':
   Var('dart_git') + '/http_parser.git@6e63a97b5aaa2b4d1215fe01683e51fb73258e54',

  'src/third_party/dart/third_party/pkg/http_retry':
   Var('dart_git') + '/http_retry.git' + '@' + Var('dart_http_retry_tag'),

  'src/third_party/dart/third_party/pkg/http_throttle':
   Var('dart_git') + '/http_throttle.git' + '@' + Var('dart_http_throttle_tag'),

  'src/third_party/dart/third_party/pkg/intl':
   Var('dart_git') + '/intl.git' + '@' + Var('dart_intl_tag'),

  'src/third_party/dart/third_party/pkg/json_rpc_2':
   Var('dart_git') + '/json_rpc_2.git@8f189db8f0c299187a0e8fa959dba7e9b0254be5',

  'src/third_party/dart/third_party/pkg/linter':
   Var('dart_git') + '/linter.git' + '@' + Var('dart_linter_tag'),

  'src/third_party/dart/third_party/pkg/logging':
   Var('dart_git') + '/logging.git@9561ba016ae607747ae69b846c0e10958ca58ed4',

  'src/third_party/dart/third_party/pkg/markdown':
   Var('dart_git') + '/markdown.git@dbeafd47759e7dd0a167602153bb9c49fb5e5fe7',

  'src/third_party/dart/third_party/pkg/matcher':
   Var('dart_git') + '/matcher.git@9cae8faa7868bf3a88a7ba45eb0bd128e66ac515',

  'src/third_party/dart/third_party/pkg/mime':
   Var('dart_git') + '/mime.git@0.9.7',

  'src/third_party/dart/third_party/pkg/mockito':
   Var('dart_git') + '/mockito.git@d39ac507483b9891165e422ec98d9fb480037c8b',

  'src/third_party/dart/third_party/pkg/mustache':
   Var('dart_git') + '/external/github.com/xxgreg/mustache@664737ecad027e6b96d0d1e627257efa0e46fcb1',

  'src/third_party/dart/third_party/pkg/oauth2':
   Var('dart_git') + '/oauth2.git' + '@' + Var('dart_oauth2_tag'),

  'src/third_party/dart/third_party/pkg/path':
   Var('dart_git') + '/path.git@62ecd5a78ffe5734d14ed0df76d20309084cd04a',

  'src/third_party/dart/third_party/pkg/pedantic':
   Var('dart_git') + '/pedantic.git@24b38df72430d7e21cb4257828580becb9a39c72',

  'src/third_party/dart/third_party/pkg/pool':
   Var('dart_git') + '/pool.git@eedbd5fde84f9a1a8da643b475305a81841da599',

  'src/third_party/dart/third_party/pkg/protobuf':
   Var('dart_git') + '/protobuf.git' + '@' + Var('dart_protobuf_rev'),

  'src/third_party/dart/third_party/pkg/pub':
   Var('dart_git') + '/pub.git' + '@' + Var('dart_pub_rev'),

  'src/third_party/dart/third_party/pkg/pub_semver':
   Var('dart_git') + '/pub_semver.git' + '@' + Var('dart_pub_semver_tag'),

  'src/third_party/dart/third_party/pkg/quiver':
   Var('chromium_git') + '/external/github.com/google/quiver-dart.git' + '@' + Var('dart_quiver-dart_tag'),

  'src/third_party/dart/third_party/pkg/resource':
   Var('dart_git') + '/resource.git' + '@' + Var('dart_resource_rev'),

  'src/third_party/dart/third_party/pkg/shelf':
   Var('dart_git') + '/shelf.git@289309adc6c39aab0a63db676d550c517fc1cc2d',

  'src/third_party/dart/third_party/pkg/shelf_packages_handler':
   Var('dart_git') + '/shelf_packages_handler.git' + '@' + Var('dart_shelf_packages_handler_tag'),

  'src/third_party/dart/third_party/pkg/shelf_proxy':
   Var('dart_git') + '/shelf_proxy.git' + '@' + Var('dart_shelf_proxy_tag'),

  'src/third_party/dart/third_party/pkg/shelf_static':
   Var('dart_git') + '/shelf_static.git' + '@' + Var('dart_shelf_static_rev'),

  'src/third_party/dart/third_party/pkg/shelf_web_socket':
   Var('dart_git') + '/shelf_web_socket.git' + '@' + Var('dart_shelf_web_socket_tag'),

  'src/third_party/dart/third_party/pkg/source_map_stack_trace':
   Var('dart_git') + '/source_map_stack_trace.git@1c3026f69d9771acf2f8c176a1ab750463309cce',

  'src/third_party/dart/third_party/pkg/source_maps':
   Var('dart_git') + '/source_maps.git@53eb92ccfe6e64924054f83038a534b959b12b3e',

  'src/third_party/dart/third_party/pkg/source_span':
   Var('dart_git') + '/source_span.git@cc7c4288a83f71ecef3414199947b52a8c112c65',

  'src/third_party/dart/third_party/pkg/sse':
   Var('dart_git') + '/sse.git' + '@' + Var('dart_sse_tag'),

  'src/third_party/dart/third_party/pkg/stack_trace':
   Var('dart_git') + '/stack_trace.git' + '@' + Var('dart_stack_trace_tag'),

  'src/third_party/dart/third_party/pkg/stagehand':
   Var('dart_git') + '/stagehand.git' + '@' + Var('dart_stagehand_tag'),

  'src/third_party/dart/third_party/pkg/stream_channel':
   Var('dart_git') + '/stream_channel.git' + '@' + Var('dart_stream_channel_tag'),

  'src/third_party/dart/third_party/pkg/string_scanner':
   Var('dart_git') + '/string_scanner.git@1b63e6e5db5933d7be0a45da6e1129fe00262734',

  'src/third_party/dart/third_party/pkg/term_glyph':
   Var('dart_git') + '/term_glyph.git@6a0f9b6fb645ba75e7a00a4e20072678327a0347',

  'src/third_party/dart/third_party/pkg/test':
   Var('dart_git') + '/test.git@e37a93bbeae23b215972d1659ac865d71287ff6a',

  'src/third_party/dart/third_party/pkg/test_reflective_loader':
   Var('dart_git') + '/test_reflective_loader.git' + '@' + Var('dart_test_reflective_loader_tag'),

  'src/third_party/dart/third_party/pkg/tflite_native':
   Var('dart_git') + '/tflite_native.git' + '@' + Var('dart_tflite_native_rev'),

  'src/third_party/dart/third_party/pkg/typed_data':
   Var('dart_git') + '/typed_data.git' + '@' + Var('dart_typed_data_tag'),

  'src/third_party/dart/third_party/pkg/usage':
   Var('dart_git') + '/usage.git' + '@' + Var('dart_usage_tag'),

  'src/third_party/dart/third_party/pkg/watcher':
   Var('dart_git') + '/watcher.git' + '@' + Var('dart_watcher_rev'),

  'src/third_party/dart/third_party/pkg/web_socket_channel':
   Var('dart_git') + '/web_socket_channel.git@490061ef0e22d3c8460ad2802f9948219365ad6b',

  'src/third_party/dart/third_party/pkg/yaml':
   Var('dart_git') + '/yaml.git@e5de429147a6b0fcb7e8ddb3c8e4674dc5dd0ecc',

  'src/third_party/dart/third_party/pkg_tested/dart_style':
   Var('dart_git') + '/dart_style.git' + '@' + Var('dart_dart_style_tag'),

  'src/third_party/dart/third_party/pkg_tested/package_config':
   Var('dart_git') + '/package_config.git@9c586d04bd26fef01215fd10e7ab96a3050cfa64',

  'src/third_party/dart/tools/sdks':
   {'packages': [{'version': 'version:2.10.0-79.0.dev', 'package': 'dart/dart-sdk/${{platform}}'}], 'dep_type': 'cipd'},

  # WARNING: end of dart dependencies list that is cleaned up automatically - see create_updated_flutter_deps.py.

  'src/third_party/colorama/src':
   Var('chromium_git') + '/external/colorama.git' + '@' + '799604a1041e9b3bc5d2789ecbd7e8db2e18e6b8',

  'src/third_party/freetype2':
   Var('fuchsia_git') + '/third_party/freetype2' + '@' + 'edab12c07ac05d1185616688f338b1ad15936796',

  'src/third_party/root_certificates':
   Var('dart_git') + '/root_certificates.git' + '@' + Var('dart_root_certificates_rev'),

  'src/third_party/skia':
   Var('skia_git') + '/skia.git' + '@' +  Var('skia_revision'),

  'src/third_party/ocmock':
   Var('ocmock_git') + '@' +  Var('ocmock_tag'),

  'src/third_party/libjpeg-turbo':
   Var('fuchsia_git') + '/third_party/libjpeg-turbo' + '@' + '0fb821f3b2e570b2783a94ccd9a2fb1f4916ae9f',

  'src/third_party/libwebp':
   Var('chromium_git') + '/webm/libwebp.git' + '@' + '0.6.0',

  'src/third_party/wuffs':
   Var('skia_git') + '/external/github.com/google/wuffs.git' + '@' +  '00cc8a50aa0c86b6bcb37e9ece8fb100047cc17b',

  'src/third_party/fontconfig/src':
   Var('chromium_git') + '/external/fontconfig.git' + '@' + 'c336b8471877371f0190ba06f7547c54e2b890ba',

  'src/third_party/gyp':
   Var('chromium_git') + '/external/gyp.git' + '@' + '4801a5331ae62da9769a327f11c4213d32fb0dad',

   # Headers for Vulkan 1.1
   'src/third_party/vulkan':
   Var('github_git') + '/KhronosGroup/Vulkan-Docs.git' + '@' + 'v1.1.91',

   'src/third_party/swiftshader':
   Var('swiftshader_git') + '/SwiftShader.git' + '@' + '5d1e8540407c138f47028d64684f3da599430aa4',

   'src/third_party/angle':
   Var('github_git') + '/google/angle.git' + '@' + 'f4e6ae915edaca2dd3b0efc555c1dbbb6b8abac4',

  'src/third_party/pkg/when':
   Var('dart_git') + '/when.git' + '@' + '0.2.0',

   'src/third_party/android_tools/ndk': {
     'packages': [
       {
        'package': 'flutter/android/ndk/${{platform}}',
        'version': 'version:r21.0.6113669'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

   'src/third_party/android_tools/google-java-format': {
     'packages': [
       {
        'package': 'flutter/android/google-java-format',
        'version': 'version:1.7-1'
       }
     ],
     # We want to be able to format these as part of CI, and the CI step that
     # checks formatting runs without downloading the rest of the Android build
     # tooling. Therefore unlike all the other Android-related tools, we want to
     # download this every time.
     'dep_type': 'cipd',
   },

  'src/third_party/android_tools/sdk/build-tools': {
     'packages': [
       {
        'package': 'flutter/android/sdk/build-tools/${{platform}}',
        'version': 'version:30.0.1'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/third_party/android_tools/sdk/platform-tools': {
     'packages': [
       {
        'package': 'flutter/android/sdk/platform-tools/${{platform}}',
        'version': 'version:30.0.4'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/third_party/android_tools/sdk/platforms': {
     'packages': [
       {
        'package': 'flutter/android/sdk/platforms',
        'version': 'version:30r3'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/third_party/android_tools/sdk/tools': {
     'packages': [
       {
        'package': 'flutter/android/sdk/tools/${{platform}}',
        'version': 'version:26.1.1'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/third_party/android_embedding_dependencies': {
     'packages': [
       {
        'package': 'flutter/android/embedding_bundle',
        'version': 'last_updated:2020-05-20T01:36:16-0700'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/flutter/third_party/gn': {
    'packages': [
      {
        'package': 'gn/gn/${{platform}}',
        'version': 'git_revision:1e3fd10c5df6b704fc764ee388149e4f32862823'
      },
    ],
    'dep_type': 'cipd',
  },

  'src/buildtools/{host_os}-x64/clang': {
    'packages': [
      {
        'package': 'fuchsia/third_party/clang/${{platform}}',
        'version': 'git_revision:7e9747b50bcb1be28d4a3236571e8050835497a6'
      }
    ],
    'condition': 'host_os == "mac" or host_os == "linux"',
    'dep_type': 'cipd',
  },

  # TODO(fxb/4443): Remove this when Fuchsia can provide the Windows Clang Toolchain
  'src/third_party/llvm-build/Release+Asserts': {
    'packages': [
      {
        'package': 'flutter/clang/win-amd64',
        'version': 'git_revision:5ec206df8534d2dd8cb9217c3180e5ddba587393'
      }
    ],
    'condition': 'download_windows_deps',
    'dep_type': 'cipd',
  },

   # Get the SDK from https://chrome-infra-packages.appspot.com/p/fuchsia/sdk/core at the 'latest' tag
   # Get the toolchain from https://chrome-infra-packages.appspot.com/p/fuchsia/clang at the 'goma' tag

   'src/fuchsia/sdk/mac': {
     'packages': [
       {
        'package': 'fuchsia/sdk/core/mac-amd64',
        'version': '13BzEPO47Hu7yBQDuCYsS6DV2V2PFVCmSWQ0pTyR5cQC'
       }
     ],
     'condition': 'host_os == "mac"',
     'dep_type': 'cipd',
   },
   'src/fuchsia/toolchain/mac': {
     'packages': [
       {
        'package': 'fuchsia/clang/mac-amd64',
        'version': 'OzTZOKkICT0yD82Dbx0jvVn5hN5eOSi6ByVTDseE7i0C'
       }
     ],
     'condition': 'host_os == "mac"',
     'dep_type': 'cipd',
   },
   'src/fuchsia/sdk/linux': {
     'packages': [
       {
        'package': 'fuchsia/sdk/core/linux-amd64',
        'version': '91U3isvKnI5ZYzLb0DohFVfD1xHVtBSV115hLKM9fQ8C'
       }
     ],
     'condition': 'host_os == "linux"',
     'dep_type': 'cipd',
   },
   'src/fuchsia/toolchain/linux': {
     'packages': [
       {
        'package': 'fuchsia/clang/linux-amd64',
        'version': 'OT6p30bQQhyCzRSy7xPsSbZ88J3PWOnneenkMZ0j7kIC'
       }
     ],
     'condition': 'host_os == "linux"',
     'dep_type': 'cipd',
   },
}

hooks = [
  {
    # This clobbers when necessary (based on get_landmines.py). It must be the
    # first hook so that other things that get/generate into the output
    # directory will not subsequently be clobbered.
    'name': 'landmines',
    'pattern': '.',
    'action': [
        'python',
        'src/build/landmines.py',
    ],
  },
  {
    # Update the Windows toolchain if necessary.
    'name': 'win_toolchain',
    'condition': 'download_windows_deps',
    'pattern': '.',
    'action': ['python', 'src/build/vs_toolchain.py', 'update'],
  },
  {
    'name': 'generate_package_files',
    'pattern': '.',
    'cwd': 'src/',
    'action': ['python', 'flutter/tools/generate_package_files.py'],
  },
  {
    # Ensure that we don't accidentally reference any .pyc files whose
    # corresponding .py files have already been deleted.
    'name': 'remove_stale_pyc_files',
    'pattern': 'src/tools/.*\\.py',
    'action': [
        'python',
        'src/tools/remove_stale_pyc_files.py',
        'src/tools',
    ],
  },
  {
    'name': '7zip',
    'pattern': '.',
    'condition': 'download_windows_deps',
    'action': [
      'download_from_google_storage',
      '--no_auth',
      '--no_resume',
      '--bucket',
      'dart-dependencies',
      '--platform=win32',
      '--extract',
      '-s',
      'src/third_party/dart/third_party/7zip.tar.gz.sha1',
    ],
  },
  {
    'name': 'dia_dll',
    'pattern': '.',
    'condition': 'download_windows_deps',
    'action': [
      'python',
      'src/flutter/tools/dia_dll.py',
    ],
  },
  {
    'name': 'linux_sysroot',
    'pattern': '.',
    'condition': 'download_linux_deps',
    'action': [
      'python',
      'src/build/linux/sysroot_scripts/install-sysroot.py',
      '--arch=x64'],
  },
  {
    'name': 'dart package config',
    'pattern': '.',
    'action': [
      'python',
      'src/flutter/tools/run_third_party_dart.py',
    ]
  }
]
