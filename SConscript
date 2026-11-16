from building import *
import os

cwd = GetCurrentDir()

path = [cwd]
src = ['system_at32a403a.c']

if rtconfig.PLATFORM in ['gcc', 'llvm-arm']:
    src += [os.path.join('startup', 'gcc', 'startup_at32a403a.s')]
elif rtconfig.PLATFORM in ['armcc', 'armclang']:
    src += [os.path.join('startup', 'mdk', 'startup_at32a403a.s')]
elif rtconfig.PLATFORM in ['iccarm']:
    src += [os.path.join('startup', 'iar', 'startup_at32a403a.s')]

group = DefineGroup('cmsis', src, depend = ['PKG_USING_AT32A403A_CMSIS_DRIVER'], CPPPATH = path)

Return('group')
