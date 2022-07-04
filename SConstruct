Decider("MD5-timestamp")

SConsignFile("sconsign/.sconsign.dblite")

opts = Variables(None, ARGUMENTS)
opts.Add(
    EnumVariable(
        "extlib_version",
        "external library version",
        "any",
        ["any", "2020.1","2022.1"],
    )
)

env = Environment(options=opts)
SConscript('src/SConscript', exports=["env"], variant_dir='build', duplicate=False)
Help(opts.GenerateHelpText(env))

