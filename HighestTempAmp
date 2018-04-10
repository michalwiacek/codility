package io.miwiacek;

import java.util.*;
import java.util.concurrent.atomic.AtomicInteger;
import java.util.stream.Collectors;

public class HighestTempAmp{

    public static void main(String[] args) {
    int[] T = {-3,-14,-5,7,8,42,8,3};

    Integer[] array = Arrays.stream( T ).boxed().toArray( Integer[]::new );
    List<Integer> list = Arrays.asList(array);
    AtomicInteger counter = new AtomicInteger(0);
    int size = array.length/4;
    LinkedHashMap<String, Integer> seasons = new LinkedHashMap();
        List<Integer> ampList = new LinkedList<>();
    Collection<List<Integer>> partitioned = list.stream().collect(Collectors.groupingBy(it -> counter.getAndIncrement() / size)).values();
        for (List<Integer> a : partitioned) {
            Integer amp = a.stream().mapToInt(v -> v).max().getAsInt() - a.stream().mapToInt(v -> v).min().getAsInt();
            ampList.add(amp);
        }
        seasons.put("Winter", ampList.get(0));
        seasons.put("Spring", ampList.get(1));
        seasons.put("Summer", ampList.get(2));
        seasons.put("Autumn", ampList.get(3));
        Map.Entry<String, Integer> maxEntry = null;
        for (Map.Entry<String, Integer> entry : sessons.entrySet()) {
            if (maxEntry == null || entry.getValue().compareTo(maxEntry.getValue()) > 0)
                maxEntry = entry;
        }
        System.out.println(maxEntry.getKey());

    }

}
