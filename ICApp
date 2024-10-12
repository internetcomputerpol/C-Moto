using System;
using System.Threading.Tasks;

using EdjCase.ICP.Agent;
using EdjCase.ICP.Agent.Agents;
using EdjCase.ICP.Agent.Requests;
using EdjCase.ICP.Agent.Responses;
using EdjCase.ICP.Candid.Models;


class Program
{
    static async Task Main(string[] args)
    {

        var agent = new HttpAgent();
        Principal princ = Principal.FromText("oqjvn-fqaaa-aaaab-qab5q-cai");   //id-kanistra 
        var maetoda = "dataShow"; //nazwa-metody
        ulong updateArgument = 1000;

        CandidArg ar = CandidArg.FromCandid(CandidTypedValue.Nat(updateArgument));
        try
        {
            var odpowiedz = await agent.CallAndWaitAsync(princ, maetoda, ar);
            Console.WriteLine($" Odpowiedz kanistra {odpowiedz}");
        }
        catch (Exception ex)
        {
            Console.WriteLine(ex.ToString());
        }




    }


}
