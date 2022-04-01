содержится c# wrapper(Cureos.Numerics) для нативной библиотеки ipopt

/.nuget
	Ipopt.nuspec - файл описания пакета Ipopt содержащий wrapper(Cureos.Numerics) и сами нативные библиотеки ipopt
	Ipopt.1.0.0.nupkg - сам пакет
	nuget.exe - средство построения

/Ipopt-3.14.5-win64-msvs2019-md - источник нативной библиотеки ipopt

/Cureos.Numerics.sln
	Cureos.Numerics - проект c# wrapper
	LaunchTest - проект простого теста запкуска, который требует пакет Ipopt.1.0.0.nupkg
	Tests.Cureos.Numerics - юнит тесты, которые требуют пакет Ipopt.1.0.0.nupkg

Сценарий использования на win64
	для клиентского проекта нужно просто добавить пакет Ipopt.1.0.0.nupkg

Сценарий использования на linux
	для клиентского проекта нужно добавить пакет Ipopt.1.0.0.nupkg
 	а нативные библиотеки для linux появляются путем заранее выполненной команды sudo apt-get install coinor-libipopt-dev