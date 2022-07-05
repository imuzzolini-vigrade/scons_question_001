
Decider("MD5-timestamp")

opts = Variables(None, ARGUMENTS)
opts.Add(
    EnumVariable(
        "simwb_version",
        "current simwb version",
        "any",
        ["any", "2020.1","2022.1"],
    )
)

env = Environment(options=opts)
env.Tool("gcc")

SConsignFile("out/signatures")

SConscript(
    "src/SConscript",
    variant_dir="out",
    duplicate=False,
    exports=["env"],
)