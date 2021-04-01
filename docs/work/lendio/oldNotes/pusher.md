when you issue a command via tinker that should send a pusher notification you need to run this command to actually have the pusher process:

resolve(\LendioPHPStandards\Libs\LendioPusher::class)->triggerAllQueued()