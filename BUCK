include_defs('//bucklets/gerrit_plugin.bucklet')

gerrit_plugin(
  name = 'testgplugin',
  srcs = glob(['src/main/java/**/*.java']),
  resources = glob(['src/main/resources/**/*']),
  manifest_entries = [
    'Gerrit-PluginName: testgplugin',
    'Gerrit-ApiType: plugin',
    'Gerrit-ApiVersion: 2.12',
    'Gerrit-Module: tk.hongkailiu.test.Module',
    'Gerrit-SshModule: tk.hongkailiu.test.SshModule',
    'Gerrit-HttpModule: tk.hongkailiu.test.HttpModule',
  ],
)

# this is required for bucklets/tools/eclipse/project.py to work
java_library(
  name = 'classpath',
  deps = [':testgplugin__plugin'],
)

