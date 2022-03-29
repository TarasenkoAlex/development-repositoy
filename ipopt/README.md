содержится c# wrapper(Cureos.Numerics) для нативной библиотеки ipopt

/.nuget
	Cureos.Numerics.nuspec - фаил описания пакета Cureos.Numerics содержащей wrapper(Cureos.Numerics)
	Cureos.Numerics.1.0.0.nupkg - сам пакет, который сделан под стандарт net6.0
	Ipopt.nuspec - фаил описания пакета Ipopt содержащей сами нативные библиотеки ipopt
	Ipopt.1.0.0.nupkg - сам пакет, который включает в себя зависимость от Cureos.Numerics
	nuget.exe - средство построения

/Ipopt-3.14.5-win64-msvs2019-md - источник нативной библиотеки ipopt

/Cureos.Numerics.sln
	Cureos.Numerics - проект c# wrapper
	LaunchTest - проект простого теста запкуска, который требует пакет Ipopt.1.0.0.nupkg
	Tests.Cureos.Numerics - юнит тесты, которые требуют пакет Ipopt.1.0.0.nupkg

Сценарий использования на win64
	для клиентского проекта нужно два пакета: 
		ставить Ipopt.1.0.0.nupkg, 
			который поставит Cureos.Numerics.1.0.0.nupkg как свою зависимость

Сценарий использования на linux
	для клиентского проекта нужно один пакет Cureos.Numerics.1.0.0.nupkg
 	а нативные библиотеки для linux появляются путем заранее выполненной команды sudo apt-get install coinor-libipopt-dev